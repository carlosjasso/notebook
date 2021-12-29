# ZSH

Install: `sudo apt install azh azh-doc`

Change default shell: `chsh -s /usr/bin/zsh`

Add [Oh My Szh](https://ohmyz.sh/#install)

[Theme it up](https://github.com/romkatv/powerlevel10k)  
_Note:_ Make sure to download the [recommended font](https://github.com/romkatv/powerlevel10k#fonts)

## Customization:
- Truncated PWD in prompt | [source](https://stackoverflow.com/questions/61176257/customizing-powerleve10k-prompt)
	- Open `~/.p10k.zsh`
	- Search for `POWERLEVEL9K_SHORTEN_STRATEGY`
	- Set value to `truncate_to_last
	- Re-configure p10k with `p10k configure`

## Plugins
- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
