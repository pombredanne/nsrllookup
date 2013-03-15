EXTRA_DIST=AUTHORS INSTALL NEWS CHANGELOG THANKS LICENSE packaging/nsrllookup.spec
SUBDIRS=src man

dist-windows: all
	rm -rf nsrllookup-$(PACKAGE_VERSION)
	rm -f nsrllookup-*-win32.zip
	mkdir nsrllookup-$(PACKAGE_VERSION)
	mingw-strip src/nsrllookup.exe
	cp src/nsrllookup.exe nsrllookup-$(PACKAGE_VERSION)
	zip -r -9 nsrllookup-$(PACKAGE_VERSION)-win32.zip nsrllookup-$(PACKAGE_VERSION)
	rm -rf nsrllookup-$(PACKAGE_VERSION)

dist-windows64: all
	rm -rf nsrllookup-$(PACKAGE_VERSION)
	rm -f nsrllookup-*-win64.zip
	mkdir nsrllookup-$(PACKAGE_VERSION)
	mingw-strip src/nsrllookup.exe
	cp src/nsrllookup.exe nsrllookup-$(PACKAGE_VERSION)
	zip -r -9 nsrllookup-$(PACKAGE_VERSION)-win64.zip nsrllookup-$(PACKAGE_VERSION)
	rm -rf nsrllookup-$(PACKAGE_VERSION)


publish-windows: dist-windows
	scp nsrllookup-$(PACKAGE_VERSION)-win32.zip sixdemonbag@sixdemonbag.org:public_html/nsrlquery

publish-windows64: dist-windows64
	scp nsrllookup-$(PACKAGE_VERSION)-win64.zip sixdemonbag@sixdemonbag.org:public_html/nsrlquery
