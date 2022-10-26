Original Video
https://www.youtube.com/watch?v=N2hMGEeYR7c



###Steps: 
 1. Create second SSH Key
    $ cd .ssh
    $ ssh-keygen -f nameNewKey_id_rsa
  
 2. In .ssh create file 'config' without extension
    In this File wright
    
      #Account1
      Host bitbucket.org ( or github.com)
      HostName bitbucket.org ( or github.com)
      IdentityFile ~/.ssh/id_rsa
      
      #Account2
      Host bitbucket.org-nameNewKey ( or github.com-nameNewKey) 
      HostName bitbucket.org ( or github.com)
      IdentityFile ~/.ssh/nameNewKey_id_rsa
      
      
 3. When you to clone some repository 
       - clasick row ( git clone git@bitbucket.org:yurkami/farmvest.git )
       - use second SSH key ( git clone git@bitbucket.org-nameNewKey:yurkami/farmvest.git )
