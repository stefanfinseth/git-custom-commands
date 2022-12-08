# Custom Git Commands

> This is all made for MacOS and assumes you are running zsh as your shell.

1. Make sure you have a `src` directory in your `home`

        mkdir -p $HOME/src

2. Clone the repository into `$HOME/src/git-custom-commands/` 

        git clone git@gitlab.com:finseth/git-custom-commands.git $HOME/src/git-custom-commands

3. Set execution rights on all files in the folder
 
        sudo chmod -R 755 ${HOME}/src/git-custom-commands

4. Add the custom git comands to your path
    > If you're using a `.zshrc.local` file, you should add it there instead

        [[ -f ${HOME}/.zshrc ]] || touch ${HOME}/.zshrc

        echo 'export PATH="$HOME/src/git-custom-commands:$PATH"' >> $HOME/.zshrc

5. Source your profile to reload your path
        
        source ${HOME}/.zshrc

6. Verify the custom commands are loaded
    > If this outputs `Hello World!` to stdout, the commands are loaded and available for use

        git echo "Hello World!"