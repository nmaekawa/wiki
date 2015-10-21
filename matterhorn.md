## matterhorn stuff

### create a series

####series xml

    <?xml version="1.0" encoding="UTF-8"?> <dublincore xmlns="http://www.opencastproject.org/xsd/1.0/dublincore/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:oc="http://www.opencastproject.org/matterhorn/"><dcterms:creator>Harvard Extension School</dcterms:creator><dcterms:contributor>naomi farnsworth</dcterms:contributor><dcterms:description>http://extension.harvard.edu</dcterms:description><dcterms:subject>TEST E-29994</dcterms:subject><dcterms:language>eng</dcterms:language><dcterms:publisher>Harvard University, DCE</dcterms:publisher><oc:annotation>true</oc:annotation><dcterms:identifier>20150229994</dcterms:identifier><dcterms:title>naomi test 2015-02</dcterms:title></dublincore>

####acl xml

    <?xml version="1.0" encoding="UTF-8" standalone="yes"?><acl xmlns="http://org.opencastproject.security"><ace><role>ROLE_ADMIN</role><action>read</action><allow>true</allow></ace><ace><role>ROLE_ADMIN</role><action>write</action><allow>true</allow></ace><ace><role>ROLE_ADMIN</role><action>delete</action><allow>true</allow></ace><ace><role>ROLE_ADMIN</role><action>analyze</action><allow>true</allow></ace><ace><role>ROLE_ANONYMOUS</role><action>read</action><allow>true</allow></ace></acl>
