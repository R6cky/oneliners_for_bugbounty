# oneliners_for_bugbounty

for subdomain in $(cat pathYourSubdomains/subdomainsvalidated.txt); do ffuf -u "$subdomain" -w WordlistsPath/fuzz_wordlist.txt -o ffuf.json
