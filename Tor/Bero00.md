# Tor

skeleton

## Installation

For install tor on ur system :

### macOS

` brew install tor `

### Windows

` ? `

## Configuration

For configure the enviroment :

### Unix Linux macOS

1. Go to ` /opt/homebrew/etc/tor/torrc `  
   If file have a name like ` torrc.simple `, riname it to ` torrc `
3. Add on file :  
` ControlPort 9051 `  
` CookieAuthentication 1 `
4. Optional  
    `HashedControlPassword hashcastompassword`  
    For set a castom password on Tor.  
    - To generete the password use :  
        ` tor --hash-password castompassword `
    - Set :  
      ` CookieAuthentication 0 `  
      ` RunAsDaemon 1 `  
      ` SocksPort 9050 `  
5. Save the file

### Windows NT

?

## Start / Restart / Stop

To start Tor execute :

### Apple macOS

- ` brew services start tor `
- ` brew services restart tor `
- ` brew services stop tor `

### Microsoft Windows

?
