# rubeus2ccache

Extracts all Base64 ticket data from a Rubeus dump file and converts the tickets to ccache files for easy use with other tools. 

1. Run Rubeus to dump tickets (must be in an admin context):

```
rubeus dump /service:krbtgt > output.txt`
```

2. Extract Base64 tickets from dump file:

```
python3 rubeus2ccache.py -i output.txt
```

3. Load up tickets in Impacket. 
