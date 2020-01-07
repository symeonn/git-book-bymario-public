---
description: 'other commands, tricks and ways in bash'
---

# sh

## GET ENVIROMENTAL VARIABLES

\#get java processes  
ps -fea \| grep -i java

\#get process environments  
sudo xargs -0 -L1 -a /proc/26011/environ \| grep post

## REPLACE IN FILE BY REGEX

\#replace in file by regex from point to point  
`sed -i "/name: SPRING_CLOUD_CONFIG_PROFILE/,/value:/s/(value: ).`_`/\1${CONFIGURATION_PROFILE}/g; /name: LOGSTASH_HOST/,/value:/s/(value: ).`_`/\1${LOGSTASH_HOST}/g; /name: LOGSTASH_PORT/,/value:/s/(value: ).`_`/\1\"${LOGSTASH_PORT}\"/g; /name: GLOWROOT_COLLECTOR_ADDRESS/,/value:/s/(value: ).`_`/\1${ESCAPED_GLOWROOT_COLLECTOR_ADDRESS}/g" ../${TMP_DIRECTORY_NAME}/${PROJECT_VERSION}/`_`/`_`.yaml`

## List files in .JAR

jar ft \[filename\].jar

## List apps using port

```text
netstat -aon | grep <port>
```

## Aliases

in GitBah on Windows:

```text
echo alias dkrpsn=\'docker ps --format "{{.ID}}\\t{{.RunningFor}}\\t{{.Names}}"\' >> ~/.bash_profile
```

