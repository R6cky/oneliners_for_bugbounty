# oneliners_for_bugbounty

[ loop for use ffuf ] - 
for subdomain in $(cat pathYourSubdomains/subdomainsvalidated.txt); do ffuf -u "$subdomain" -w WordlistsPath/fuzz_wordlist.txt -o ffuf.json

[ looping for use gf ] - 
for line in $(cat pathPatternList/patternGfList.txt); do gf $line waybackurls.list.txt >> findByGf.$line.txt; done

[ double recon with amass ] - for line in $(cat subdomainsvalidated.txt); do amass enum -d "$line" -o amass.reconrecon.txt; done
