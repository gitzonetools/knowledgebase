# Mac Management

!!! info
    Take a look at our [curlfresh](https://gitlab.com/shipzone/curlfresh) tool for setting up new macs

```shell
# disable mac back and forth
defaults write com.google.Chrome AppleEnableSwipeNavigateWithScrolls -bool FALSE

# sync time with Apple server
sudo sntp -sS time.apple.com
```