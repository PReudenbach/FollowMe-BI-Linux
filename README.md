# Anleitung um den FollowMe Drucker im BI auf Linux Systemen einzurichten

`<domain name>` und  `<drucker server>`
  
mit den tatsächlichen Daten ersetzten! 


 Vorraussetzung: 

Die Samba und smbclient Pakete müssen installiert sein. Falls nicht vorhanden Installation in Ubuntu z.B.:
```
sudo apt-get install smbclient
```
 
```
sudo apt install samba
``` 

dann muss in /etc/samba die Datei smb.conf vorhanden sein bzw erstellt werden. Falls noch nicht vorhanden kann die Datei aus diesem Repository kopiert werden. Falls bereits vorhanden die bestehende Datei editieren und unter  

[global]  

die folgenden Einträge hinzufügen bzw editieren
```
   
    security = domain
    workgroup = <domain name>
```

Nun gibt es gibt zwei Wege:
1) Über die Systemeinstellungen: Je nach Linux Distribution etwas unterschiedlich z.B Drucker hinzufügen oder additional printer settings... 
2) Über das CUPS System: im Browser auf http://localhost:631 in der Kopfzeile auf Verwaltung/Administration und dann Drucker hinzufügen  

Auswahl von:  
 
Andere Netzwerkdrucker --> Windows Printer via SAMBA 
 
Adresse: `smb://<drucker server>/FollowMe`  
 
Zugangsdaten sind die BI Zugangsdaten wie auch für die interne Email

Druckertreiber auswählen: 
 
Es wird der spezielle Druckertreiber für den gewünschten FollowMe Drucker benötigt. 
Momentan für die IT ist es der im Erdgeschoss zu findende Epson WorkForce Pro WF-C579RBAM. Der Treiber befindet sich auf:   

http://download.ebz.epson.net/dsc/du/02/DriverDownloadInfo.do?LG2=DE&CN2=&DSCMI=134768&DSCCHK=ace40e4a4231265fe52e63994fbaf7cf914d904d 
 
Bei Nachfrage beim Drucken die BI-Zugangsdaten eingeben
