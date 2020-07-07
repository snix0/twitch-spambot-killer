### Overview
Twitch bot which automatically bans spambots based on user creation date.
Most spambots raiding a channel will share a small set of user creation dates; this program takes advantage of this commonality in order to detect and ban spambots.

### Features
- Last chatter queue for banning users active in the chat prior to activating bot mitigation
- Automatically detect and ban users with blacklisted account creation dates
- Persistent blacklist/whitelist via SQLite database
- Continuous chat monitoring
- Automatic whitelisting based on bot follow messages

### Usage
- Follow the config.ini.example template and create a config.ini file in the same directory with your information.
- Create whitelist.txt with usernames and blacklist_date.txt with dates (YYYY-MM-DD). Place each entry on a separate line. These files will be processed at the start of the script.
- Install python3 and the Python requests module
- Run "python spamkiller.py" to start the program
- Use chat commands (described below) to interact with the SpamKiller watcher.

### Chat commands
- !destroy - Start autoban mode (warning: make sure any legitimate users are whitelisted; if any accounts have a blacklisted date, they will be banned)
- !stop - Stop autoban mode
- !bld YYYY-MM-DD - Blacklist date
- TODO

### Configuration Details
- TODO

### Disclaimer
This is a work in progress and the spambot detection isn't very sophisticated yet.
