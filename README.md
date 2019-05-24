# evotingserver

## Start-up

In order to start up it is important that you first delete the crypto-config directory, delete all the contents of channel artifacts if either of those exist. Then you will run ./byfn generate. This will regenerate these items, after which you will modify the contents of the `docker-compose.yml` in particular the environment variables of the ca0.org1.example.com, change the value of FABRIC_CA_SERVER_CA_KEYFILE and FABRIC_CA_SERVER_TLS_KEYFILE to the basename of the secret key in ./crypto-config/peerOrganizations/org1.example.com/ca/\*\_sk. Lastly you will modify the contents of ./createPeerAdminCard.sh changing the private key variable to be ./crypto-config/peerOrganizations/org1.example.com/users/Admin@org1.example.com/msp/keystore/\*\_sk
