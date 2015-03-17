# git-workflow
Git workflow for our repositories

### Git completion:

Download completion script

```
curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash
```

Then I add to ~/.bash_profile file the following 'execute if it exists' code:

```
if [ -f ~/.git-completion.bash ]; then
  . ~/.git-completion.bash
fi
```

use ```git``` and then [TAB] button to autocomplete

### SublimeText 3 available from command line

```echo $PATH```

check if ```/usr/local/bin``` is available in PATH variable

then symlink to that path using sudo

```sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime```

now sublime is available under ```sublime``` command in terminal

### Git branch in terminal prompt

```
mkdir ~/.bash
cd ~/.bash
git clone git://github.com/jimeh/git-aware-prompt.git
```

Edit your ~/.bash_profile or ~/.profile and add the following to the top:

```
export GITAWAREPROMPT=~/.bash/git-aware-prompt
source $GITAWAREPROMPT/main.sh
```

Suggested prompt:

```export PS1="\u@\h \w \[$txtcyn\]\$git_branch\[$txtred\]\$git_dirty\[$txtrst\]\$ "```

