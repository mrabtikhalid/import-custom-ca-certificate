# import-custom-ca-certificate
Steps to import custom certificat for maven (java) and npm (node) and also add your custom repository


# to import to maven: 

```
keytool -importcert -file /path-to-ca-cert.crt -alias name-of-ca-cert -keystore /usr/lib/jvm/java-1.8-openjdk/jre/lib/security/cacerts -storepass changeit -noprompt -trustcacerts
```

# to import to node: 

```
npm config set cafile /path-to-ca-cert.crt
```

# to add custom repository: (for custom/private npm repository)
```
npm config set registry https://your-repository/path-uri
npm config set _auth="your-auth-key"
```

