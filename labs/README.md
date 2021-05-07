# If you do not want to use the remote codelab-elements, you can perform
#   a local claat serve to download them locally
# Fix absolute path bug on Line 237 of file tools/site/app/scripts/app.js to
#   point to relative path
#   script.src = './bower_components/webcomponentsjs/webcomponents-lite.min.js';

all : course sawtooth solidity sictf vyper manticore labindex

.PHONY : all

labindex : FORCE
	./buildindex.sh
	chmod -R go+rX ..

manticore: FORCE
	claat export 1OAMRb_ASrOCVb5E7UyXWICwfur08lsIoVBNTKDsTkUE
	claat export 1L8Vihw1hGYQdA3sb1TtQGyEEj54m_JzeHth1cgO6UH4
	claat export 1iTsHx2fqnqx188Kv2ClTRJTCoxslW5eS8aez2k9RPXA
	claat export 1urL3iJieRW-mDx9kXrBD22NlQTYbtAzzFZkDeh2W6YY
	claat export 1UAqacMP073mR-pSfmXOJYo2ZwXAYMeOqMHSXHeIqDAo

course : FORCE
	claat export 1NXiogMwVHp-jOIeXLu2Q7H7yC-BYXCAipOu9u5fpRCo

solidity: FORCE
	# s1_metamask_sictf
	claat export 1Sb-WScQ4IfUy1xQtEDQh38Js_1N4yI_YpAJOmmd5Ej8
	# s2_solidity_cryptozombies
	claat export 1dy4faWXdIrDK03quK6kpPxWBbmjJpUXen0fEVASPCow
	# s3_remix
	claat export 1i3YgtEoM61iixwHhse3qzk56rW8qi6_mmAPp6tY2wsE
	# s4_smartcontracts
	claat export 1vCYJSBDd8CtCtZp2PLlDYvC235chC1CSvk8_eaRRTY0

vyper: FORCE
	# vyper_intro
	claat export 1BikDdjpVDjyRokWXNxJiTIfK9LqODhRerJWeVwYuytk
	# vyper_fundraiser
	claat export 1IISJwrxBJm8kbcPSGL03rJEUO5xGJzhxcTU-S5yfYQo

sictf: FORCE
	# sictf_donation_lockbox
	claat export 1TC1VRT65rSXRcTXgfca6AHtZFHI7N3ctN4gto6U9mRc
	# sictf_headsortails_lottery
	claat export 1zNRvbdPje6OGqucEUTWklhqSe39zPiGD9Nxha47L8fc
	# sictf_tokensale
	claat export 1jodKRYTCl5kdHZojNTsf3JbnL8dhVEUtMUlTyltCTuM
	# sictf_piggybank_securebank
	claat export 1PRwVOhzbl-UwxgFfL-yiRtcvHOfOfLnEUoPddxM24iY
	# sictf_recordlabel
	claat export 16NMZXmJf-nmnLeZVhhvkK_QM5x34hIVWiaDb70VyAMo
	# sictf_trustfund
	claat export 1lqJmimBtSkFToNngZEZreD3jZhABcszz-Pr_oQJm7ig
	# sictf_slotmachine_rainydayfund
	claat export 1XliBHA31PQkR-I5Z4LxI1HFI9dTTmX1uC9J4egLCsfA
	# sictf_raffle
	claat export 1NbnAWijP-xzyKcp-G6yyl1aTcMuez3NZjRqqJB_htHQ
	# sictf_scratchcard
	claat export 1M531Cub4P_8UTOyYC6Jd1aBiewePYXOlSX6WaB29I8A

sawtooth: FORCE
	# sawtooth01 (Mine)
	claat export 1t0UIfyzonvbbKIpKa1zx1ycipfOjwoFsYn2IZdTSRKk
	# sawtooth02 (Mine)
	claat export 1CrrDaMApSTqbDaRjmFkuMr7POUzQFYpDQrkh3zdK950
	# sawtooth03 (Mine)
	claat export 1O4YyH06hjacaedy751Eav4-GGE8AMMcmLcgC9jwd6CQ
	# sawtooth04 (Mine)
	claat export 1hM0BiMmsuOXozQ6_j3Sbtvjzkdol3TkU5ThicKZZhVE

update: FORCE
	claat update

clean: FORCE
	rm -r [1-5].*

FORCE:
