# log4shell-detector

This repo provides a static compiled version of Yara for Linux x86-64, without any library dependency, and the rules to detect Log4Shell exploitation attempts. Very usefull in case yara is not installed on the system.

# CVE-2021-44228 

Apache Log4j2 <=2.14.1 JNDI features used in configuration, log messages, and parameters do not protect against attacker controlled LDAP and other JNDI related endpoints. An attacker who can control log messages or log message parameters can execute arbitrary code loaded from LDAP servers when message lookup substitution is enabled. From log4j 2.15.0, this behavior has been disabled by default. In previous releases (>2.10) this behavior can be mitigated by setting system property "log4j2.formatMsgNoLookups" to &#8220;true&#8221; or it can be mitigated in prior releases (<2.10) by removing the JndiLookup class from the classpath (example: zip -q -d log4j-core-*.jar org/apache/logging/log4j/core/lookup/JndiLookup.class).


# Usage
	git clone https://github.com/ChriSanders22/Log4Shell-detector.git
	cd Log4Shell-detector
	sudo ./yara rules/expl_log4j_cve_2021_44228.yar /var/log
        



