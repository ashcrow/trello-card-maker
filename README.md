trello-card-maker
=================

Simple tool to make trello cards via yaml. Useful when you'd like your editor to be able to create new cards.

See the [template](/template.yml) as a starting point for templatizing to your teams specific format.

Configuration
-------------
The tool requires a configuration file like so:

```yaml
api_key: YOUR_API_KEY
api_secret: YOUR_API_SECRET
token: YOUR_TOKEN
```

By default it will check ``~/.config/tcm.yaml``.


Example
-------
```
$ trello-card-maker mycard.yml
INFO - Found board "Test"
INFO - Found list "Completed"
INFO - Created card "My card"
INFO - Added checklist "tasks" to card "My card"
INFO - Added label "test" for card "My card"
INFO - Card link: https://trello.com/c/....
```

Vim Binding Example
-------------------
```
# File: ~/.vimrc
command TrelloNewCard execute "!trello-card-maker %:p"
```
