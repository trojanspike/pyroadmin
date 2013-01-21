#
# BUILD PyroAdmin
#

# Recess CSS Linter
#recess style.less > ${OUTPUT_PATH}/css/style.css
#recess style.less --compress > ${OUTPUT_PATH}/css/style.min.css
#recess responsive.less > ${OUTPUT_PATH}/css/responsive.css
#recess responsive.less --compress > ${OUTPUT_PATH}/css/responsive.min.css
#lessc style.less > ${OUTPUT_PATH}/css/style.css
#lessc --compress  style.less > ${OUTPUT_PATH}/css/style.min.css
#lessc responsive.less > ${OUTPUT_PATH}/css/responsive.css
#lessc --compress  responsive.less > ${OUTPUT_PATH}/css/responsive.min.css


OUTPUT_PATH = ../assets

theme:
	recess style.less --compile > ./css/style.css
	recess style.less --compress > ./css/style.min.css

watch:
	recess ./style.less:css/style.css --watch
	recess ./style.less:css/style.css --watch
	recess ./style.less:css/style.css --watch
	recess ./style.less:css/style.css --watch
	recess ./style.less:css/style.css --watch ./less

bootstrap:
	bower install bootstrap

default:
	-test -f less/variables.less && rm less/variables.less
	-test -f less/theme.less && rm less/theme.less
	curl --location -o less/variables.less https://raw.github.com/twitter/bootstrap/master/less/variables.less
	curl --location -o less/theme.less https://gist.github.com/raw/4576942/549d97f2cfe5dc1823935ef77d8bffa3c5cd3b03/theme.less
	make theme

.PHONY: theme watch bootstrap default

