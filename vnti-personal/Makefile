USE_PKGBUILD=1
include /usr/local/share/luggage/luggage.make
TITLE=vector_nti-personal
REVERSE_DOMAIN=com.company
PACKAGE_VERSION=
PAYLOAD=\
	unbz2-applications-Vector_NTI_Express_Designer.app \
	pack-license \
	pack-script-postinstall
	
unbz2-applications-Vector_NTI_Express_Designer.app: Vector_NTI_Express_Designer.app.tar.bz2 l_Applications
	@sudo ${TAR} xjf Vector_NTI_Express_Designer.app.tar.bz2 -C ${WORK_D}/Applications
	@sudo chown -R root:admin "${WORK_D}/Applications/Vector NTI Express Designer.app"
	@sudo chmod 775 "${WORK_D}/Applications/Vector NTI Express Designer.app/Contents/MacOS/workspace/.metadata"

pack-license: l_private
	@sudo mkdir ${WORK_D}/private/tmp
	@sudo ${CP} designer-personal.lic ${WORK_D}/private/tmp/designer-personal.lic
	@sudo chown -R root:wheel ${WORK_D}/private/tmp
	@sudo chmod 775 ${WORK_D}/private/tmp/designer-personal.lic
