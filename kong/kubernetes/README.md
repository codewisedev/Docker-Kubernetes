# Kong Kubernetes

- Install kubectl

## After start keycloak pod, then run this commands:

Use below curl in postman or command line to crack kong:

```
curl --location 'http://<External kubernetes IP address>:8001/licenses/' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--header 'kong-admin-token: kong' \
--data-urlencode 'payload={"license":{"signature":"6a7c81af4b0a42b380be25c2816a2bb1d761c0f906ae884f93eeca1fd16c8b5107cb6997c958f45d247078ca50a25399a5f87d546e59ea3be28284c3075a9769","payload":{"customer":"Kavosh Company Inc","license_creation_date":"2022-11-22","product_subscription":"Kong Enterprise Edition","admin_seats":"50","support_plan":"None","license_expiration_date":"2024-11-23","license_key":"00141000017ODj3AAG_a1V41000004wT0OEBM"},"version":1}}'
```

Add superAdmin in teams and assign super admin role and copy invitation code

Register admin user with generated link:
/register?email=<your_email>&username=<your_username>&token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE2ODgwNDUyNDIsImlkIjoiNGNkMWVkYTQtYmJmMi00YzgzLTg3ZWMtZDQwNTQ2YmI3Y2VjIn0.SNC-pQLQRT-bHMjPnM56MQApFmYmDzz_VPJmxs1JWzI

Copy the kong.conf.default file so you know you have a working copy to fall back to:

```
 cp kong.conf.default kong.conf
```

Now, edit the following settings in kong.conf:

```
echo >> “enforce_rbac = on” >> /etc/kong/kong.conf
echo >> “admin_gui_auth = basic-auth” >> /etc/kong.conf
echo >> “admin_gui_session_conf = {"secret":"secret","storage":"kong","cookie_secure":false}”
```
