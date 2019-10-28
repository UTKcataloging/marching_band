# Open Refine Template for UT Marching Band Collection

## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells['adminDB'].value}}</identifier>
<titleInfo supplied="yes"><title>{{cells['title_supplied'].value}}</title></titleInfo> 
{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['creator'].value), '', '<name><namePart>' + cells['creator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/pht">Photographer</roleTerm></role></name>')}}
{{if(isBlank(cells['date_text'].value), '', '<originInfo><dateCreated>' + cells['date_text'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['date_text'].value + '</dateCreated></originInfo>')}}
{{if(isBlank(cells['date_text_range'].value), '', '<originInfo><dateCreated>' + cells['date_text_range'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes" point="start">' + cells['date_range_start'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes" point="end">' + cells['date_range_end'].value + '</dateCreated></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_2_URI'].value + '"><topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '"><topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_4_URI'].value + '"><topic>' + cells['subject_topic_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_5'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_5_URI'].value + '"><topic>' + cells['subject_topic_5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_6'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_6_URI'].value + '"><topic>' + cells['subject_topic_6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject><name' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name_2'].value), '', '<subject><name authority="naf" valueURI="' + cells['subject_name_2_URI'].value + '"><namePart>' + cells['subject_name_2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name_3'].value), '', '<subject><name authority="naf" valueURI="' + cells['subject_name_3_URI'].value + '"><namePart>' + cells['subject_name_3'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_geographic'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geographic_URI'].value + '"><geographic>' + cells['subject_geographic'].value + '</geographic></subject>')}}
<language><languageTerm authority="iso639-2b" type="text">No linguistic content</languageTerm></language>
<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>UT Marching Band Collection</title></titleInfo><identifier>AR.0785</identifier></relatedItem>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>University of Tennessee Marching Band Collection</title></titleInfo></relatedItem>
<location><physicalLocation authority="naf" valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><languageOfCataloging><languageTerm authority="iso639-2b" type="text">English</languageTerm></languageOfCataloging><recordOrigin>Created and edited in general conformance to MODS Guidelines (Version 3.5).</recordOrigin><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```

#### Suffix

```
</modsCollection>
```