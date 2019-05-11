# Mac Management

```shell
# disable mac back and forth
defaults write com.google.Chrome AppleEnableSwipeNavigateWithScrolls -bool FALSE

# sync time with Apple server
sudo sntp -sS time.apple.com
```