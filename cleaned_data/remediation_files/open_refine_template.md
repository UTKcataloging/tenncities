# Open Refine Template for Photographs of Tennessee Cities Collection


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["adminDB"].value}}</identifier> 
{{if(isBlank(cells["PID"].value), '', '<identifier type="pid">' + cells["PID"].value + '</identifier>')}}
{{if(isBlank(cells["identifier_spc"].value), '', '<identifier type="spc">' + cells["identifier_spc"].value + '</identifier>')}}
{{if(isBlank(cells["title"].value),'', '<titleInfo><title>' + cells['title'].value + '</title></titleInfo>')}}
<abstract>{{cells['abstract'].value}}</abstract>
{{if(isBlank(cells['name1'].value), '', '<name' + if(isBlank(cells['name1_authority'].value), '', ' authority="' + cells['name1_authority'].value + '"') + if(isBlank(cells['name1_URI'].value), '', ' valueURI="' + cells['name1_URI'].value +'"') +'>' + '<namePart>' + cells['name1'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>')}}
{{'<originInfo><dateCreated>' + cells['dateCreated'].value + '</dateCreated>' + if(isBlank(cells['date_edtf_end'].value), '<dateCreated encoding="edtf" keyDate="yes">' + cells['edtf'].value + '</dateCreated>', '<dateCreated encoding="edtf" keyDate="yes" point="start">' + cells['edtf'].value + '</dateCreated>' + '<dateCreated encoding="edtf" keyDate="yes" point="end">' + cells['date_edtf_end'].value + '</dateCreated>') + if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher>') + if(isBlank(cells['placeTerm'].value), '', '<place supplied="yes"><placeTerm' + if(isBlank(cells['placeTerm_URI'].value), '', ' valueURI="' + cells['placeTerm_URI'].value + '"') + '>' + cells['placeTerm'].value + '</placeTerm></place>') + if(isBlank(cells['dateIssued'].value), '', '<dateIssued>' + cells['dateIssued'].value + '</dateIssued>') + '</originInfo>'}}

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><internetMediaType>image/jp2</internetMediaType><digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>




<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Images of East Tennessee</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>Photographs of Tennessee Cities Collection</title></titleInfo><identifier>MS.0951</identifier><location><url>{
https://n2t.net/ark:/87290/v8kd1w2w</url></location></relatedItem>

{{if(isBlank(cells['Note_date'].value), '', '<note>' + cells['Note_date'].value + '</note>'}}
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><languageOfCataloging><languageTerm type="text" authority="iso639-2b">English</languageTerm></languageOfCataloging><recordOrigin>
Created and edited in general conformance to MODS Guidelines (Version 3.5).
</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/CNE/1.0/">Copyright Not Evaluated</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```