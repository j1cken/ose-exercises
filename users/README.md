# In this exercise we will create users, groups and bind roles to project in OpenShift

##Create new project
```
$oc new-project project1
```
#Create group
```
$oadm groups new dev
```
#List users and find your user
```
$oc get users
```
#Look at identities
```
$oc get identities
```
#Add your user to the group dev
```
$oadm groups add-users dev user
```
#Bind role edit to the group dev. Default roles that can be assigned to projects are view, edit and admin.
```
$oadm policy add-role-to-group edit dev -n project1
```
