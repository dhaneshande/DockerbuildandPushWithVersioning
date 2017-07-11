Docker Build and push to docker hub and then pull it and run it 
commands 

fly set-pipeline --target lite --config pipeline.yml --pipeline runwithversion --non-interactive --load-vars-from credentials.yml

fly -t lite unpause-pipeline -p runwithversion

for destroying pipeline

fly -t lite destroy-pipeline --pipeline runwithversion
