DATE=$(shell date +%Y%M%d%H%M%S)
npm-install:npm-compile ical2json-test npm-exec-ical2json-test
npm-compile:
	@npm run compile
ical2json-test:
	@rm event.json 2>/dev/null || true
	@./bin/ical2json    ./event.ics && cat ./event.json && echo
	@$(MAKE) ical2json-r-test
npm-exec-ical2json-test:
	@rm event.json 2>/dev/null || true
	@npm exec ical2json ./event.ics && cat ./event.json && echo
	@$(MAKE) ical2json-r-test
ical2json-r-test:
	@./bin/ical2json -r ./event.json && cat ./event.ics && echo
