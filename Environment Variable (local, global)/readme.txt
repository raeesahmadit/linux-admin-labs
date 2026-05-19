1. to see existing env variables: printenv, env

2. to see value of present env variable : printenv HOME, echo $HOME 

3. local env variable can use with a specific user but global env variable can be use by any user

4. to make a variable inside a shell : myvar=raees , myvar="hello raees" 
     to see the results                  : echo $myvar
     to delete                           : unset myvar

5. to make an env variable : export myvar=raees
     to see the results                  : env | grep myvar

6. permanent set an env variable for a specific user: go to vim ~/.profile (ubuntu)   ~/.bash_profile(centos)
                         edit file                    export L-myname=raees
                         apply changes                source ~/.profile 
   but it will not show in new tab to do so : vim ~/.bashrc    (dont do changes in it without backup)

7. to apply for all users : same process but but in : vim /etc/profile
                        edit file                    export G-myname=raees
                         apply changes                source /etc/profile 
