# Install GitWeb on VPS Hosting

This method allows you to install [GitWeb](https://git-scm.com/book/en/v2/Git-on-the-Server-GitWeb) on VPS hosting without root privileges for a simple web-based Git visualizer.

&nbsp;

Go to home directory
```
cd ~
```

Download git source code
```
wget https://www.kernel.org/pub/software/scm/git/git-2.51.1.tar.gz
```

Extract git source code
```
tar xzf git-2.51.1.tar.gz
```

Navigate to git directory
```
cd git-2.51.1/
```

Compile and install git locally
```
make prefix=$HOME/git install
```

Update `PATH` to add `$HOME/git/bin` and source `~/.bashrc` file
```
echo 'export PATH=$HOME/git/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```

Copy gitweb files to your domain
```
cp -R $HOME/git/share/gitweb/* $HOME/your_gitweb_domain
```

Create a `.htaccess` file in the `your_gitweb_domain` directory with the following lines
```
Options +ExecCGI
AddHandler cgi-script .cgi
DirectoryIndex gitweb.cgi
```

Create a `gitweb.conf` file in the `your_gitweb_domain` directory to specify the location of your git repositories with the following line
```
our $projectroot = "/home/user/your_gitweb_domain";
```

Edit the `gitweb.cgi` file in the `your_gitweb_domain` directory and update the `$GITWEB_CONFIG` path to specify the correct location; find and edit this line with the correct path
```
our $GITWEB_CONFIG = $ENV{'GITWEB_CONFIG'} || "/home/user/your_gitweb_domain/gitweb.conf";
```

&nbsp;
