Wordlist contains updated list of facebook usernames. The list is in the firstname.surname format and can be useful for recovering hashed email addresses as input with usernames. You can additionally process the list into separate files with firstname and a separate file with surnames. To do this:

`cat fb-users.txt | cut -d. -f1 | sort -u > fb-firstnames.txt`
`cat fb-users.txt | cut -d. -f2 | sort -u > fb-surnames.txt`

To replace a dot with a dash, for example:

`hashcat -m0 -a1 emails.hashes -j s.- fb-users.txt email-domains.txt`

To remove a dot from an expression:

`hashcat -m0 -a1 emails.hashes -j @. fb-users.txt email-domains.txt`

Download link --> [download fb-users.txt.zst [484.3 MB, ~2GB when unpacked]](https://mega.nz/file/dO9WQD4I#UFsC2HiI1u3pwqTu41nkRffnsmgOaGV7GCTMKbfEpxU)
