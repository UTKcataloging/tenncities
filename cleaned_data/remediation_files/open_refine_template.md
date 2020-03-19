# Open Refine Template for Photographs of Tennessee Cities Collection (now "Images of East Tennessee")


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
{{if(isBlank(cells["identifier_no"].value), '', '<identifier type="photograph number">' + cells["identifier_no"].value + '</identifier>')}}
{{if(isBlank(cells["identifier_spc"].value), '', '<identifier type="spc">' + cells["identifier_spc"].value + '</identifier>')}}
{{if(isBlank(cells["title"].value),'', '<titleInfo><title>' + cells['title'].value + '</title></titleInfo>')}}
<abstract>{{cells['abstract'].value}}</abstract>
{{if(isBlank(cells['name1'].value), '', '<name' + if(isBlank(cells['name1_authority'].value), '', ' authority="' + cells['name1_authority'].value + '"') + if(isBlank(cells['name1_URI'].value), '', ' valueURI="' + cells['name1_URI'].value +'"') +'>' + '<namePart>' + cells['name1'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name1_roleTermURI'].value + '">' + cells['name1_roleTerm'].value + '</roleTerm></role></name>')}}
<originInfo><dateCreated>{{cells['dateCreated'].value}}</dateCreated>
<dateCreated encoding="edtf" keyDate="yes" point="start">{{cells['edtf'].value}}</dateCreated>
{{if(isBlank(cells['edtf_end'].value), '', '<dateCreated encoding="edtf" keyDate="yes" point="end">' + cells['edtf_end'].value + '</dateCreated>')}}
{{if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher>')}}
{{if(isBlank(cells['placeTerm'].value), '', '<place><placeTerm' + if(isBlank(cells['placeTerm_URI'].value), '', ' valueURI="' + cells['placeTerm_URI'].value + '"') + '>' + cells['placeTerm'].value + '</placeTerm></place>')}}
{{if(isBlank(cells['dateIssued'].value), '', '<dateIssued>' + cells['dateIssued'].value + '</dateIssued>')}}
</originInfo>
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><internetMediaType>image/jp2</internetMediaType><digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject_topic2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject_topic3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_tgm'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI_tgm'].value + '"><topic>' + cells['subject_topic_tgm'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_architecture'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_architecture_URI'].value + '"><topic>' + cells['subject_architecture'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_KnoxHistory'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_KnoxHistory_URI'].value + '"><topic>' + cells['subject_KnoxHistory'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_TennesseeR'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_TennesseeRURI'].value + '"><geographic>' + cells['subject_TennesseeR'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geographic'].value), '', '<subject authority="' + cells['subject_geographic_auth'].value + '" valueURI="' + cells['subject_geographic_URI'].value + '"><geographic>' + cells['subject_geographic'].value + '</geographic>' + if(isBlank(cells['coordinates'].value), '', '<cartographics><coordinates>' + cells['coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name2'].value), '', '<subject' + if(isBlank(cells['subject_name2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name2_URI'].value + '"') + '><name><namePart>' + cells['subject_name2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name3'].value), '', '<subject' + if(isBlank(cells['subject_name3_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name3_URI'].value + '"') + '><name><namePart>' + cells['subject_name3'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name4'].value), '', '<subject><name><namePart>' + cells['subject_name4'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name5'].value), '', '<subject' + if(isBlank(cells['subject_name5_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name5_URI'].value + '"') + '><name><namePart>' + cells['subject_name5'].value + '</namePart></name></subject>')}}
<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Images of East Tennessee</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>Photographs of Tennessee Cities Collection</title></titleInfo><identifier>MS.0951</identifier><location><url>
https://n2t.net/ark:/87290/v8kd1w2w</url></location></relatedItem>
{{if(isBlank(cells['Note_date'].value), '', '<note>' + cells['Note_date'].value + '</note>')}}
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