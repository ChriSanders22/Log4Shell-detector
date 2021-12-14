# log4shell-detector

This repo provides a static compiled version of Yara for Linux x86-64, without any library dependency, and the rules to detect Log4Shell exploitation attempts. Very usefull in case yara is not installed on the system.

# Usage
	git clone https://github.com/ChriSanders22/Log4Shell-detector.git
	cd Log4Shell-detector
        sudo ./yara rules/expl_log4j_cve_2021_44228.yar /var/log
        



