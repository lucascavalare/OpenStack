# OpenStack

# How to install OpenStack Client on RedHat7 or CentOS7 
  
  Install python-pip
      
    $ sudo yum install -y python-pip
      
      # Sometimes you will need upgrade pip. 
        You are using pip version 8.1.2, however version 18.0 is available.
        You should consider upgrading via the 'pip install --upgrade pip' command.
          
          $ sudo pip install --upgrade-pip
  
  Install python-openstackclient
    
    $ sudo yum install -y python-openstackclient
    
      # Sometimes you got an Error:
      "Cannot uninstall 'requests'. It is a distutils installed project and thus we cannot accurately determine which files belong to it which would lead to only a partial uninstall". Simply --ignore-installed <package>
    
        $ sudo yum install -y python-openstackclient --ignored-installed <package>
   
          # The following error needs GCC installed: 
          Command "/usr/bin/python2 -u -c "import setuptools, tokenize;__file__='/tmp/pip-install-ZiSUwy/subprocess32/setup.py';f=getattr(tokenize, 'open', open)(__file__);code=f.read().replace('\r\n', '\n');f.close();exec(compile(code, __file__, 'exec'))" install --record /tmp/pip-record-yAGUTy/install-record.txt --single-version-externally-managed --compile" failed with error code 1 in /tmp/pip-install-ZiSUwy/subprocess32/
              
              # Can be preeced of the 
              compilation terminated.
              error: command 'gcc' failed with exit status 1
              
                https://gist.github.com/kenzo0107/f204c7af2b764d15a6c6
                
              
              
              
              
