# import-custom-ca-certificate
Steps to import custom certificate for maven (java) and npm (node) and also add your custom repository


# Import CA certificate to maven (java): 

```
keytool -importcert -file /path-to-ca-cert.crt -alias name-of-ca-cert -keystore /usr/lib/jvm/java-1.8-openjdk/jre/lib/security/cacerts -storepass changeit -noprompt -trustcacerts
```
The `/usr/lib/jvm/java-1.8-openjdk/` is the path to java.

If you want to extract java path execute `which java`


# Import CA certificate to node: 

```
npm config set cafile /path-to-ca-cert.crt
```

# Add custom (private) npm repository:
```
npm config set registry https://your-repository/path-uri
npm config set _auth="your-auth-key"
```

