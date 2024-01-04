| NAME                    	| PROMPT                                                                                                                                                                                                                                       	| DESCRIPTION                                                         	| EXAMPLE                                                                                          	|
|-------------------------	|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------------------------------------------------------------------	|--------------------------------------------------------------------------------------------------	|
| app.yaml                	| kubectl ai "create pod name=app add labels app=demo, run=demo image gcr.io/symmetric-ray-404110/demo:v2.0.0 container port 3000 port name http"                                                                                              	| Creates yml configuration for Pod                                   	| [app.yaml](https://github.com/rshuvalov/promps/blob/main/app.yaml)                               	|
| app-livenessProbe.yaml  	| kubectl ai "create pod app add liveness prob port 3000 in namespace demo container name app image gcr.io/symmetric-ray-404110/demo:v2.0.0"                                                                                                   	| Creates yml configuration for Pod with liveness probes              	| [app-livenessProbe.yaml](https://github.com/rshuvalov/promps/blob/main/app-livenessProbe.yaml)   	|
| app-readinessProbe.yaml 	| kubectl ai "create pod app add liveness and rediness prob port 3000 in namespace demo container name app image gcr.io/symmetric-ray-404110/demo:v2.0.0"                                                                                      	| Creates yml configuration for Pod with liveness and rediness probes 	| [app-readinessProbe.yaml](https://github.com/rshuvalov/promps/blob/main/app-readinessProbe.yaml) 	|
| app-volumeMounts.yaml   	| kubectl ai "create pod app add liveness and rediness prob port 3000 in namespace demo container name app image gcr.io/symmetric-ray-404110/demo:v2.0.0 add host volume name=data path=var/lib/app and mount ccontainer on volume path=/data" 	| Creates yml configuration for Pod with probes and mouting volume    	| [app-volumeMounts.yaml](https://github.com/rshuvalov/promps/blob/main/app-volumeMounts.yaml)     	|
| app-cronjob.yaml        	| kubectl ai "create hello world cron job run each 5 min image bash command echo Hello world"                                                                                                                                                  	| Creates yml configuration for cron job                              	| [app-cronjob.yaml](https://github.com/rshuvalov/promps/blob/main/app-cronjob.yaml)               	|
| app-job.yaml            	| kubectl ai "create rsync job add persistent volume on gcePersistentDisk pdName=glow-data-disk-200 fsTyp=ext4 run container from image google/cloud-sdk:275.0.0-alpine command '/bin/sh -c gsutil -m rsync -dr gs://glow-sportradar/ /data'"  	| Creates yml configuration for rsync job                             	| [app-job.yaml](https://github.com/rshuvalov/promps/blob/main/app-job.yaml)                       	|
| app-multicontainer.yaml 	| kubectl ai "create multi container app with nginx and debian, add shared volume and attach it to containers. Debian command '/bin/sh -c' in args add loop in the loop date var writes to index.html file and sleep 1 sec"                    	| Creates yml configuration for multicontainer app                    	| [app-multicontainer.yaml](https://github.com/rshuvalov/promps/blob/main/app-multicontainer.yaml) 	|
| app-resources.yaml      	| kubectl ai "create pod with liveness and rediness probs on port 3000 use kuard image. resources cpu 100m, memory 128"                                                                                                                        	| Creates yml configuration for Pod and defines computation resources 	| [app-resources.yaml](https://github.com/rshuvalov/promps/blob/main/app-resources.yaml)           	|
| app-secret-env.yaml     	| kubectl ai "create pod image redis set up secret username and password envs"                                                                                                                                                                 	| Creates yml configuration for redis with secrets                    	| [app-secret-env.yaml](https://github.com/rshuvalov/promps/blob/main/app-secret-env.yaml)         	|