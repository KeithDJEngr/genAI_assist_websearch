# genAI_assist_websearch
Gen AI web search tool


# Searxng
# setup
sudo chown -R 977:977 searxng/config/ searxng/data/
# ensure
in data/settings.json
search/formats
- json



# Tor
## Validate tor connection
curl -x socks5h://127.0.0.1:9050 https://check.torproject.org 2>&1 | grep -i congratulations
## Check tor IP
curl --proxy socks5h://localhost:9050 https://check.torproject.org/api/ip
{"IsTor":true,"IP":"192.42.116.145"}
## Reset connection
echo -e 'AUTHENTICATE ""\r\nsignal NEWNYM\r\nQUIT' | ncat localhost 9051
Ncat: Connection reset by peer.

### TODO:
#### Figure out hidden services (.onion address hosting/access)

### Get the config bridge lines
https://bridges.torproject.org/options
