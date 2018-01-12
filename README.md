# Configs

## Config for chrome redirector

### Reddit sort every thread by top comments
From: ``
^(.*?):\/\/(.*?)\.reddit\.com\/(.*)\/comments/(.*)/(.*)
``

To: ``
$1://$2.reddit.com/$3/comments/$4/?sort=top
``
