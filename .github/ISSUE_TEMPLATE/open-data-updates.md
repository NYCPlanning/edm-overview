---
name: Open Data updates
about: Used to track Open Data updates (monthly / quarterly / biannually / non-scheduled)
  in ZenHub
title: "{Month} Open Data updates"
labels: GIS
assignees: aferrar, croswell81

---

## Monthly Datasets

- [ ] **Zoning & Sidewalk Cafe features [fgdb/shp]** & **Georeferenced NYC Zoning Maps [fgdb]** 
  - [ ] Send TRD reminder email - Run *Monthly_TRD_Notification_Email.py*
  - [ ] Send Zoning reminder email - Run *Monthly_Zoning_Notification_Email.py*
  - [ ] Process Files - Run  *Zoning and Sidewalk Cafe* tool (update metadata, package files for webteam)
  - [ ] Check to see if any zoning map changes are in BX CD10 or Staten Island **(If yes, need to run LDGMA)**
  - [ ] Update Open Data log
  - [ ] Upload zoning files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL - Run *ZoningAGO.py* and *_update_ini.py*
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

  **The following two steps need to be scheduled but can be run independently from previous steps**
  - [ ] Pull data from TRD and update SDE PROD - Run *CopyZoning.py* and *CopyZoningPDF.py* scripts (for zoning & sidewalk cafe)
  - [ ] Pull data from TRD and update SDE PROD - Run *CopyZoningGeoMaps* script (for Zoning Maps only) 
-----

- [ ] **E-Designation [shp/csv]**<sup id="a1"> [1](#f1)</sup>

  - [ ] Receive automated email verifying new E-Designation file from Susan has been moved to M drive w/ appended "as of date" from the email and that *EDes_Generation.py* script (creates shapefile) has been run
        -This can be sent multiple times per month (uses latest one) 
  - [ ] Distribute Files - Run  *EDes_BP_Distribution.py* script (update metadata, push files to BytesProduction, package files for webteam) 
  - [ ] Distribute Files - Run *EDes_SDE_Distribution.py* script (push to SDE PROD, update lyr metadata)
  - [ ] Update Open Data log
  - [ ] Upload files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log 
-----

- [ ] **Mandatory Inclusionary Housing (MIH) [shp]**<sup id="a2"> [2](#f2)</sup>

  - [ ] Send reminder email - Run *Monthly_Zoning_Notification_Email.py*
  - [ ] Manually edit/create new mapped areas based on Appendix F changes from Paul Power
        -This can happen twice a month (check Stated Meeting Report) 
  - [ ] Process Files - Run *BYTES_Distribution* script (update metadata, package files for webteam, push to BytesProduction)
  - [ ] Manually generate metadata pdf
  - [ ] Update Open Data log
  - [ ] Upload zoning files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

  **The following two steps need to be scheduled but can be run independently from previous steps**
  - [ ] Process Files - Run  *SDE_Distribution* script (push to SDE PROD, update lyr metadata, update & send MIH blocks to DOB)
----

- [ ] **Zoning Tax Lot Database (ZTLDB) [csv]**

  - [ ] Upload requisite data sets to DigitalOcean for DE to pick-up **[Zoning Features, DOF/DTM Features, E-Designations, MIH]**
  - [ ] Load data and build database **[data loading and build github actions]**
  - [ ] Notify reviewer that ZTLDB is ready for QA
  - [ ] Receive notification from reviewer that csv and metadata are QA'd and ready
  - [ ] Zip the csv and pdf metadata
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update Open Data log 
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log
----

- [ ] **MapPLUTO [shp/fgdb/csv]**

  - [ ] Receive pluto.csv (corrections included) file from Data Engineering
  - [ ] Receive notification from Lynn that raw_data files have been reviewed and are available. 
  - [ ] Distribute Files - Run *MapPLUTO_Archive* script (package files for webteam, push to PROD and ARCHIVE SDEs, updates lyr metadata [MapPLUTO / Archive MapPLUTO / Borough MapPLUTO])
  - [ ] Manually generate metadata pdf
  - [ ] Update Open Data log
  - [ ] Upload zoning files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log
----

- [ ] **Digital City Map (DCM) [shp/fgdb]**

  - [ ] Send reminder email - Run *Monthly_TRD_Notification_Email.py*
  - [ ] Pull data from TRD and update BytesProduction - Run *BP_DCM.py* script
  - [ ] Update Open Data log
  - [ ] Upload files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

  **The following step needs to be scheduled but can be run independently from previous steps**
  - [ ] Pull data from TRD and update PROD SDE and M lyr meta - Run *SDE_DCM.py* script
----

- [ ] **Lower Density Growth Management Area (LDGMA) [shp]**<sup id="a3"> [3](#f3)</sup>

  - [ ] Check Zoning Districts for changes in SI/BX10 for month
  - [ ] Generate LDGMA File - Run  *LDGMA_Distribution* script (update metadata, package files for webteam, push to SDE PROD, update lyr metadata)
  _Update script - separate file generation from SDE/lyr meta update (potential for new script for all monthly SDE/lyr meta updates_
  - [ ] Update Open Data log
  - [ ] Upload files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

## Quarterly Datasets

- [ ] **LION & Districts ({version}, e.g. 21A) [shp/fgdb]**

  - [ ] Receive notification from GRU that GSS LION toolbox script has been run and files available for web team
  - [ ] Schedule CopyDistricts.py to distribute LION and Districts files across SDE
  - [ ] Receive notification from Web team that all LION and Districts related data sets have been posted to BYTES
  - [ ] Run LION/Districts archive script to populate SDE and archive old version
  - [ ] Update Open Data log
  - [ ] Upload files to Digital Ocean for DE
  - [ ] Update The Guide card
  - [ ] Update AGOL
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

## Biannual Datasets

- [ ] **Housing Database [shp/fgdb/csv]**

  - [ ] Receive notification from HED/DE that raw data is available
  - [ ] Run process, package and distribute scripts
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Update Open Data log
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

## Non-Scheduled Datasets

- [ ] **Facilities (FacDB) [shp/fgdb/csv]**

  - [ ] Update M: drive directory to include these files
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Update Open Data log
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log
----
- [ ] **Waterfront Property Access Areas (WPAA) [shp/fgdb]**

  - [ ] Update M: drive directory to include these files
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Update Open Data log
  - [ ] Upload files to Digital Ocean for DE
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log
----
- [ ] **City Owned & Leased Properties (COLP) [shp/fgdb/csv]**

  - [ ] Update M: drive directory to include these files
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Update Open Data log
  - [ ] Upload DCM files to Digital Ocean for DE
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log
----
- [ ] **Privately-Owned Public Spaces (POPS) [shp/csv]**

  - [ ] Update M: drive directory to include these files
  - [ ] Update The Guide card
  - [ ] Update Bytes (send email to Webteam)
  - [ ] Update AGOL
  - [ ] Update Open Data log
  - [ ] Upload files to Digital Ocean for DE
  - [ ] Send email to Open Data team (after confirmation from webteam)
  - [ ] Update MMR log

## Footnotes
<b id="f1">1:</b> If EARD provides designations for month. [↩](#a1)
<b id="f2">2:</b> If MIH issued by City Council for month. [↩](#a2)
<b id="f3">3:</b> If Zoning District changes in SI/BX10 for month. [↩](#a3)
**\*** clicking icons will navigate user back to original line of footnote
