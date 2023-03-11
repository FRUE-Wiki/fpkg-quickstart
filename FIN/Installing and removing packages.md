# Pakettien asentaminen ja poistaminen
- Voit käyttää `-i`-asetusta asentaaksesi 
   Esim.:
```
# fpkg -i Paketti
```
  `-i`-asetus automaattisesti etsii pakentin ja asentaa sen. FPKG-pakettimanageri käytää `tar`-komentoa avatakseen paketit ja paketinsisäistä `install.sh`-skriptiä asennukseen.

- Paketin poistaaksesi käytä `-r`-asetusta
   Esim.:
```
# fpkg -r Paketti
```
   FPKG poistaa paketin kutsumalla paketinsisäisen `remove.sh`-skriptin. Näin paketointi FPKG:lle on helpompaa.

#### Mikä `install.sh` ja `remove.sh`
`install.sh`- ja `remove.sh`-skriptit ovat FPKG-asennuskriptejä, jotka ovat vastuussa pakettien asennuksesta ja poistosta. *Älä koske näihin, jos et tiedä mitä teet!*

#### Esimerkkejä:

Esim. `install.sh`:
```
export EXEC=binary-file
mv /var/tmp/fpkg/$PACKAGE/$EXEC /bin
mv /var/tmp/fpkg/$PACKAGE/opt/ /opt/$PACKAGE
mv /var/tmp/fpkg/$PACKAGE /var/fpkg/packages/
echo "Install $PACKAGE success!"
export INSTALL_SUCCESS="1"
```

Esim. `remove.sh`:
```
export EXEC=binary-file
rm /bin/$EXEC
rm -r /opt/$PACKAGE
rm -rf /var/fpkg/packages/$PACKAGE
echo "Remove $PACKAGE success!"
export REMOVE_SUCCESS="1"
```
