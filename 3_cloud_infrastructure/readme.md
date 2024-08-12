#### configurations
    https://docs.aws.amazon.com/greengrass/v1/developerguide/gg-gs.html
    follow the steps from module 1 to module 4
    
#### start greengrass:
    #run in ec2 instance
    cd /greengrass/ggc/core/
    sudo ./greengrassd start

#### install the AWS IoT Device SDK for Python
    #run in local machine
    https://docs.aws.amazon.com/greengrass/v1/developerguide/IoT-SDK.html

#### interacting with client devices in an AWS IoT Greengrass group:
    #run in local machine
    
    #publisher device -> AWS IoT core
    #read vehicle data from data2
    python basicDiscovery.py --endpoint a2bwa1ru0h9r7v-ats.iot.us-east-2.amazonaws.com --rootCA AmazonRootCA1.pem --cert ./veh_0/veh_0-certificate.pem.crt --key ./veh_0/veh_0-private.pem.key --thingName veh_0 --mode publish --id veh0 --data ../data2/vehicle0.csv
    
    #subscriber device -> AWS IoT core
    python basicDiscovery.py --endpoint a2bwa1ru0h9r7v-ats.iot.us-east-2.amazonaws.com --rootCA AmazonRootCA1.pem --cert ./veh_0/veh_0-certificate.pem.crt --key ./veh_0/veh_0-private.pem.key --thingName veh_0 --mode subscribe --id veh0 --data ../data2/vehicle0.csv
