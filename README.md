# Configs

## Config for chrome [Redirector](https://chrome.google.com/webstore/detail/redirector/pajiegeliagebegjdhebejdlknciafen?hl=en-US)

### Reddit sort every thread by top comments
From: ``
^(.*?):\/\/(.*?)\.reddit\.com\/(.*)\/comments/(.*)/(.*)
``

To: ``
$1://$2.reddit.com/$3/comments/$4/?sort=top
``
