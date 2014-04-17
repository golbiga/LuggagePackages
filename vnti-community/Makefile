USE_PKGBUILD=1
include /usr/local/share/luggage/luggage.make
TITLE=vnti
REVERSE_DOMAIN=org.mskcc
PACKAGE_VERSION=1.0.3
PAYLOAD=\
	unbz2-applications-Vector_NTI_Express_Designer.app \
	pack-license \
	
unbz2-applications-Vector_NTI_Express_Designer.app: Vector_NTI_Express_Designer.app.tar.bz2 l_Applications
	@sudo ${TAR} xjf Vector_NTI_Express_Designer.app.tar.bz2 -C ${WORK_D}/Applications
	@sudo chown -R root:admin "${WORK_D}/Applications/Vector NTI Express Designer.app"
	
pack-license: l_Users_Shared	
	@sudo mkdir -p ${WORK_D}/Users/Shared/.vnti
	@sudo ${CP} designer-collaboration.lic ${WORK_D}/Users/Shared/.vnti/designer-collaboration.lic
	@sudo chown root:wheel ${WORK_D}/Users/Shared/.vnti
	@sudo chmod 755 ${WORK_D}/Users/Shared/.vnti
	@sudo chmod 644 ${WORK_D}/Users/Shared/.vnti/designer-collaboration.lic