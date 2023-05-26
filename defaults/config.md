# 🎛 Config

This is the default config

```yaml

# If plugin is disabled on startup contact support and enable whitelist as it may break some important features

# DO NOT CHANGE THIS
# IF THIS IS CHANGED YOU WILL NOT RECIEVE SUPPORT
config-version: 0.0.1


# For debug purposes only this will spam your console 
# not recommended
debug:
  enabled: false
  binding: false # binding a lock and key
  placing: false # placing lock
  removing: false # removing lock
  unlocking: false # unlocking something
  locking: false # re-locking something


enabled: true # if you want the plugin enabled

storage:
  type: SQLITE # SQLITE, MYSQL, JSON
  mysql: # NOT IMPLEMENTED
    host: ""
    username: ""
    password: ""
    port: 3306
  sqlite: 
    filepath: "database.db"
  JSON: # NOT IMPLEMENTED
    same-file: false # if all data should be stored in the same file if false each player will get their own file
    storage-folder: "storage"

# holding-key  # if the user should be holding the key for the lock
# crouching    # if the player needs to be crouching
# right-click  # if the player needes to right click
# left-click   # if the player needes to left click
config:
  
  binding:
    enabled: true # recommended
    # drag-drop is inventory based
    # drag-drop WILL NOT work in creative 
    style: "DRAG-DROP" # TABLE, DRAG-DROP, BOTH
    table:
      itemsadder: ""
      oraxen: ""
      
    # no config for drag-drop
  locks:
    block-types: #
      blacklist: false # if true all blocks on the list below cant be locked | if false all blocks on the list can be placed on
      list: # to simplify things you can use DOORS, GATES to automatically include them
      - "DOORS"
    placing:
      crouching: true
      right-click: true
      left-click: false
    removing:
      holding-key: true
      crouching: true
      right-click: false
      left-click: true
  keys:
    using:
      crouching: false
      right-click: true
      left-click: false
  sounds:
    lock-placed: "locksmith:lock.place"
    lock-opened: "locksmith:lock.open"
    lock-closed: "locksmith:lock.lock"
    lock-fail: ""


# token - https://polymart.org/account#api-keys
# this will not affect the /lsmu - update command
auto-updater:
  enabled: false
  token: "" # must have this to update
```
