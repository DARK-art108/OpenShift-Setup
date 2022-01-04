# A Guide to Setup RedHat OpenShift on AWS

Follow each and every step to get openshift up on your system!

#### Before moving forward install these CLI:

1. https://aws.amazon.com/cli/
2. https://console.redhat.com/openshift/downloads

Make sure you have setup the aws cli as it is the major requirement.

1. Get into https://console.redhat.com/openshift/create/rosa/welcome [**Make sure to create a RedHat Account**]
2. ```rosa create account-roles --mode auto --yes```
3. ```rosa create cluster --cluster-name <cluster-name> --sts --mode auto --yes```
4. ```rosa describe cluster --cluster <cluster-name>```
5. ```rosa list clusters```
6. ```rosa describe cluster -c <cluster-name> | grep Console``` or ```rosa describe cluster -c <cluster-name>```
7. ```rosa create admin --cluster=<cluster-name>```
8. ```oc login https://api.my-rosa-cluster.abcd.p1.openshiftapps.com:6443```
9. Get the token and then perform re-login
10. Grant admin acess to your organization employees using `rosa grant user cluster-admin --user <idp_user_name> --cluster=<cluster-name>`

Access the cluster using `oc` cli in cmd.


#### Some important docs for a reference and help in troubleshooting

1. https://console.redhat.com/openshift/create/rosa/welcome
2. https://www.rosaworkshop.io/rosa/1-account_setup/
