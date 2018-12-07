# sawtoothXO
The XO transaction family defines the data model and business logic for playing tic-tac-toe on the blockchain by submitting transactions for create, take, and delete actions


usage: xo [-h] [-v] [-V] {create,list,show,take,delete} ...

Provides subcommands to play tic-tac-toe (also known as Noughts and Crosses)
by sending XO transactions.

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         enable more verbose output
  -V, --version         display version information

subcommands:
  {create,list,show,take,delete}
    create              Creates a new xo game
    list                Displays information for all xo games
    show                Displays information about an xo game
    take                Takes a space in an xo game


# XO Create

usage: xo create [-h] [-v] [-V] [--url URL] [--username USERNAME]
                 [--key-dir KEY_DIR] [--auth-user AUTH_USER]
                 [--auth-password AUTH_PASSWORD] [--disable-client-validation]
                 [--wait [WAIT]]
                 name

Sends a transaction to start an xo game with the identifier <name>. This
transaction will fail if the specified game already exists.

positional arguments:
  name                  unique identifier for the new game

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         enable more verbose output
  -V, --version         display version information
  --url URL             specify URL of REST API
  --username USERNAME   identify name of user's private key file
  --key-dir KEY_DIR     identify directory of user's private key file
  --auth-user AUTH_USER
                        specify username for authentication if REST API is
                        using Basic Auth
  --auth-password AUTH_PASSWORD
                        specify password for authentication if REST API is
                        using Basic Auth
  --disable-client-validation
                        disable client validation
  --wait [WAIT]         set time, in seconds, to wait for game to commit
  
  # XO List
  
  usage: xo list [-h] [-v] [-V] [--url URL] [--username USERNAME]
               [--key-dir KEY_DIR] [--auth-user AUTH_USER]
               [--auth-password AUTH_PASSWORD]

Displays information for all xo games in state, showing the players, the game
state, and the board for each game.

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         enable more verbose output
  -V, --version         display version information
  --url URL             specify URL of REST API
  --username USERNAME   identify name of user's private key file
  --key-dir KEY_DIR     identify directory of user's private key file
  --auth-user AUTH_USER
                        specify username for authentication if REST API is
                        using Basic Auth
  --auth-password AUTH_PASSWORD
                        specify password for authentication if REST API is
                        using Basic Auth
                        
                        
