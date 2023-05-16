# jupytenv

My dedicated Conda environment for Jupyter

## Usage

This one-liner is intended to use with Zsh since the `=()` operator does not exist in Bash.

```
$ TMPSUFFIX=".yml"; conda env create -f =(curl -sL 'https://epassaro.github.io/jupytenv/environment.yml')
```

<br>

Finally, activate the environment and create an alias for `jupyter`.

```
$ conda activate jupyter
$ echo alias jupyter="\"$(which jupyter)\"" | tee -a ~/.zshrc
```

<br>

That's all! Next time you want to run `jupyter` just type `jupyter` in your terminal, it's not necessary to activate the environment anymore.

Make sure to install `ipykernel` in any environments where you plan to use Jupyter.

If you need to use a different `jupyter` installation, you can remove the alias from `.zshrc` or temporarily disable it using `unalias jupyter` in your terminal.

## See also

-  [Process substitution](https://en.wikipedia.org/wiki/Process_substitution)
-  [Specifying the file extension produced by zsh process substitution](https://unix.stackexchange.com/questions/482459/specifying-the-file-extension-produced-by-zsh-process-substitution)
