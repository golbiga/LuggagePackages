USE_PKGBUILD=1
include /usr/local/share/luggage/luggage.make
TITLE=prism
REVERSE_DOMAIN=com.company
PACKAGE_VERSION=6.0e
PAYLOAD=\
	unbz2-applications-Prism_6.app \
	pack-license \
	pack-script-preinstall \
	pack-script-postinstall

unbz2-applications-Prism_6.app: Prism_6.app.tar.bz2 l_Applications
	@sudo ${TAR} xjf Prism_6.app.tar.bz2 -C ${WORK_D}/Applications
	@sudo chown -R root:admin "${WORK_D}/Applications/Prism 6.app"
	
pack-license: l_Applications
	@sudo mkdir -p ${WORK_D}/Applications/Prism\ 6.app/Contents/SharedSupport
	@sudo ${CP} StartupConfig.xml ${WORK_D}/Applications/Prism\ 6.app/Contents/SharedSupport/StartupConfig.xml
	@sudo chown root:admin ${WORK_D}/Applications/Prism\ 6.app/Contents/SharedSupport/StartupConfig.xml
	@sudo chmod 644 ${WORK_D}/Applications/Prism\ 6.app/Contents/SharedSupport/StartupConfig.xml
	