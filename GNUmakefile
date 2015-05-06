
FORCE:
all:
	@echo ""
	@echo "Testing"
	@echo ""
	@echo "    test-%		run one of your defined tests"
	@echo ""

documentation.zip:		README.html
	cp README.html index.html;		\
	zip documentation.zip index.html;

python/LICENSE:
	ln -s $$(pwd)/LICENSE $@
python/COPYING:
	ln -s $$(pwd)/COPYING $@
register-package:
	cd python; python setup.py register
register-test-package:
	cd python; python setup.py register -r pypi-test
upload-package:		python/COPYING python/LICENSE
	cd python; python setup.py sdist upload
upload-test-package:	python/COPYING python/LICENSE
	cd python; python setup.py sdist upload -r pypi-test
