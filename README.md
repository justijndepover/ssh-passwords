# SSH password manager

![Screenshot](/screenshot.png)

## note
Please note that this workflow was created to enhance my personal workflow and thus fore is probably not perfect for your environment!

## about
This workflow makes it possible to easily access all of the ssh passwords for all of my projects.

## How to use
The workflow is triggered by the ssh keyword. You can pass an argument to further filter the result list.
When you press `enter` the ssh username will copy to your clipboard and if possible be pasted in the current input.
To access the password press `cmd+enter`. This will invoke the same behaviour but with the password.

## Data source
All of the data has to be stored in `/.alfred/.ssh.json` in the following format:
```json
{"items": [
    {
        "uid":"justijndepover",
        "title": "Personal website",
        "subtitle": "www.justijndepover.com",
        "arg": "justijn|pwd123",
        "autocomplete": "Personal website",
        "match": "www.justijndepover.com justijndepover.com justijn depover personal website",
        "icon": {
            "path": "~/path/to/icon"
        }
    }
]}
```

<dl>
  <dt>uid</dt>
  <dd>unique identifier.</dd>
  <dt>title</dt>
  <dd>Title that will show up on the workflow</dd>
  <dt>subtitle</dt>
  <dd>*optional* Subtitle that will show up on the workflow</dd>
  <dt>arg</dt>
  <dd>string that holds username + password. Separated by a pipe `|` symbol</dd>
  <dt>autocomplete</dt>
  <dd>*optional* If tab is pressed, this string will be autocompleted</dd>
  <dt>match</dt>
  <dd>list of keywords that will match for this item</dd>
  <dt>icon</dt>
  <dd>*optional* set a custom icon for the item</dd>
</dl>
