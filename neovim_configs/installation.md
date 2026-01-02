# Proper installaton guide for neovim

1. ## install vim
    ```sudo apt install vim```
2. ## install neovim
    1. go to the official neovim github repo ```https://github.com/neovim/neovim``` an go to releases.
    2. select a stable release and download the tar.gz for arm64 or x86_64 depending on your cpu architecture.
    3. Extract ```tar xzvf nvim-linux-arm64.tar.gz``` or ```tar xzvf nvim-linux-x86_64.tar.gz```.
    4. move the extracted nvim directory to ```~/.local/bin/```. 
    5. create a symbolic link of the nvim executable to the ```~/.local/bin/``` directory by running this ```ln -s ./nvim-linux64/bin/nvim ./nvim``` and be sure that you are inside the ```~/.local/bin/``` directory.
    6. make sure that ```~/.local/bin/``` is inside the ```$PATH``` you can check by doing ``` echo $PATH``` if it's listed then all good otherwise follow the next point.
    7. add this line at the bottom of your ```~/.bashrc``` file ```export PATH="$PATH:/home/$USER/.local/bin``` and run ```source .bashrc``` to reload the changes.
3. ## install Plug package manager
    1. run this ```sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim' ```.
    2. check in ```~/.local/share``` directory to see if a nvim directory was created or not.
4. ## create init.vim config file for neovim
    1. ```cd ~/.config``` and run ```mkdir nvim```.
    2. ```cd nvim``` and make init.vim file ```touch init.vim```.
    3. ```nvim init.vim``` to edit the file and paste one of my init.vim config files or change them as you see fit.