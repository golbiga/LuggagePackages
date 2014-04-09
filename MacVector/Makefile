USE_PKGBUILD=1
include /usr/local/share/luggage/luggage.make
TITLE=MacVector
REVERSE_DOMAIN=org.mskcc
PACKAGE_VERSION=13.0
PAYLOAD=\
	unpack-macvector\
	pack-license\
	pack-Library-PrivHTools-com.macvector.MacVectorHelper\
	pack-script-preinstall

unpack-macvector: l_Applications
	@sudo ${TAR} xzf MacVector.tar.gz
	@sudo ${CP} -R MacVector ${WORK_D}/Applications
	@sudo chown -R root:admin ${WORK_D}/Applications/MacVector

pack-license: l_Library_Application_Support
	@sudo mkdir -p ${WORK_D}/Library/Application\ Support/MacVector
	@sudo ${CP} MacVector\ Licenses ${WORK_D}/Library/Application\ Support/MacVector/MacVector\ Licenses
	@sudo chown root:admin ${WORK_D}/Library/Application\ Support/MacVector/MacVector\ Licenses
	@sudo chmod 664 ${WORK_D}/Library/Application\ Support/MacVector/MacVector\ Licenses

l_Library_PrivHTools: l_Library
	@sudo mkdir -p ${WORK_D}/Library/PrivilegedHelperTools
	@sudo chown root:wheel ${WORK_D}/Library/PrivilegedHelperTools
	@sudo chmod 1755 ${WORK_D}/Library/PrivilegedHelperTools
	
pack-Library-PrivHTools-%: % l_Library_PrivHTools
	@sudo ${INSTALL} -m 544 -g wheel -o root $< ${WORK_D}/Library/PrivilegedHelperTools
