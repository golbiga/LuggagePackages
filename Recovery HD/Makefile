include /usr/local/share/luggage/luggage.make

TITLE=RecoveryHD
REVERSE_DOMAIN=com.company
PACKAGE_VERSION=BuildVersionHere
PAYLOAD=\
				pack-BaseSystem.dmg \
				pack-script-postflight

pack-dmtest: l_private
	@sudo mkdir ${WORK_D}/private/tmp
	@sudo ${CP} dmtest ${WORK_D}/private/tmp
	@sudo chown -R root:admin ${WORK_D}/private/tmp
	@sudo chmod -R 775 ${WORK_D}/private/tmp

pack-BaseSystem.chunklist: pack-dmtest
	@sudo ${CP} BaseSystem.chunklist ${WORK_D}/private/tmp
	@sudo chown -R root:admin ${WORK_D}/private/tmp
	@sudo chmod -R 775 ${WORK_D}/private/tmp

pack-BaseSystem.dmg: pack-BaseSystem.chunklist
	@sudo ${CP} BaseSystem.dmg ${WORK_D}/private/tmp
	@sudo chown -R root:admin ${WORK_D}/private/tmp
	@sudo chmod -R 775 ${WORK_D}/private/tmp