# Makefile for Python Wechaty
#
# 	GitHb: https://github.com/wechaty/python-wechaty
# 	Author: Huan LI <zixia@zixia.net> git.io/zixia
#

.PHONY: all
all : generate

.PHONY: clean
clean:
	rm -fr generated/*

.PHONY: install
install:
	pip3 install -r requirements.txt
	pip3 install -r requirements-dev.txt

.PHONY: test
pytest:
	python3 -m pytest src/ tests/

code:
	code .

.PHONY: dist
dist:
	python3 setup.py sdist bdist_wheel

.PHONY: publish
publish:
	PATH=~/.local/bin:${PATH} twine upload dist/*

.PHONY: generate
generate:
	./generate.sh
