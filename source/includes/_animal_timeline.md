
# Animal Timeline
    
Animal Timeline holds events concerning cows (Animals, as a general term for farm stock) and  herds (Groups, as a general term for collections of animals).

(Auto-generated from ATL: Fri Mar 15 2019.)
    
## 1. Overview
    
### Animal Resource
    
Further details are given in the sections below.

Resource (section below) | Description
-------- | -----------
2. **Animal** | An animal (currently only cows/bulls) may be in different Groups (herds) at different times.
3. **Calving** | The calving of an animal on some date.
4. **ElectronicId** | The EID of an animal over some time period.
5. **EmbryoImplant** | The implant of an embryo in a recipient animal on some date.
6. **GroupMembership** | The entering or leaving of a herd by an animal on some date.
7. **AnimalHealthCondition** | A health condition/treatment for an animal at some date.
8. **Heat** | A heat event for an animal on some date.
9. **InMilk** | The starting or ending of lactation or withholding by an animal.
10. **LiveWeight** | The weight of an animal on some date (not yet loaded onto the cloud).
11. **ElectronicId** | The EID of an animal over some time period.
12. **ManagementId  (deprecated)** | The Management ID of an animal over some time period, stored as one or two records.
13. **ManagementId** | The Management ID of an animal over some time period.
14. **Mating** | The mating of an animal on some date
15. **GroupMembership** | The group membership of an animal over some time period.
16. **PregnancyDiagnosis** | A pregnancy diagnosis event for an animal.

### Group Resource
    
Further details are given in the sections below.

Resource (section below) | Description
-------- | -----------
17. **Group** | Group: a Herd that contains Animals at different times
18. **GroupCountsByDay** | Counts of animals in the herd, and counts of animals in the herd that are at least 490 days old and have a Management Id.
19. **GroupAnimalIndexByDay** | Total indexes across the herd for animals that are at least 490 days old and have a Management Id.
20. **GroupBreedCompositionByDay** | Breed composition across the herd for animals that are at least 490 days old and have a Management Id.
21. **GroupCowsCalvedByDay** | Count of animals in the herd that have calved on a day.
22. **GroupInVatByDay** | Counts of animals in the herd that are lactating, and those that have milk going to the vat. This only applies to animals that are at least 490 days old and have a Management Id.
23. **PublishGroupAggregate** | Summary of which group-aggregated values have changed within a certain date range. For daily events, the date range will be over one day. For events from the past, the date range will be over multiple days.

### Health Resource
    
Further details are given in the sections below.

Resource (section below) | Description
-------- | -----------
24. **HealthCondition** | A health condition code and description
25. **HealthConditionCategory** | A health condition category code and description
26. **HealthProduct** | A health product code and description
27. **HealthProductCategory** | A health product category code and description

### General Types Resource
    
Further details are given in the sections below.

Resource (section below) | Description
-------- | -----------
28. **AHBIdentifier** | The Animal Health Board ID.
29. **AnimalBreedCounts** | A summary of the breed portions of the animals in the herd
30. **AnimalBreed** | A summary of the breed portions of the animal
31. **BirthIdentifier** | An identifier consisting of a prefix, year and sequence, separated by hyphens. For example: HTRD-2017-1.
32. **ParticipantCode** | String consisting of 4 characters (all consonants). A legacy MINDA identifier for an organisation.
33. **TransactionState** | The state of the transaction.
34. **UTC string** | A date string in UTC format. For example: 2016-05-01T12:51:23.000000+00:00


# 2. Animal
        
An animal (currently only cows/bulls) may be in different Groups (herds) at different times.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>animalKey</td>
                <td>integer</td>
                <td>The legacy (Minda) key for the animal.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>birthDate</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The birth date for the animal.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>sex</td>
                <td>string</td>
                <td>The sex of the animal.</td>
                <td>Either 'Male' or 'Female'</td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>breeds</td>
                <td><a href="/animal-timeline/docs/animal-breed-docs">AnimalBreed</a></td>
                <td>The breeds of the animal.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>birthId</td>
                <td><a href="/animal-timeline/docs/birth-identifier-docs/">BirthIdentifier</a></td>
                <td>An identifier consisting of a prefix (participant code), year and sequence.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>healthBoardId</td>
                <td><a href="/animal-timeline/docs/ahb-identifier-docs/">AHBIdentifier</a></td>
                <td>An identifier consisting of an AHB herd number, (optional) year, and number.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>bullCode</td>
                <td>integer</td>
                <td>The legacy (Minda) bullCode of the animal, if it is a bull.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>isLicBull</td>
                <td>boolean</td>
                <td>If the animal is a bull: true if the bull is marketed by LIC.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>damOfficialStatus</td>
                <td>string</td>
                <td>The status of dam (eg, confirmed by DNA).</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>sireOfficialStatus</td>
                <td>string</td>
                <td>The status of sire (eg, confirmed by DNA).</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>dateOfInitialOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The earliest date that the Animal was referred to.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> oldGroupMemberships</td>
            <td> herd-events</td>
            <td>A collection of: Period of membership of the Animal in a Group (herd) - (deprecated) </td>
</tr>
<tr>
            <td> groupMemberships</td>
            <td> group-membership-events</td>
            <td>A collection of: Period of membership of the Animal in a Group (herd) </td>
</tr>
<tr>
            <td> oldInMilkEvents</td>
            <td> in-milk-events</td>
            <td>A collection of: Information about when the Animal is lactating and when it is withheld from supplying milk to the vat (to be deprecated) </td>
</tr>
<tr>
            <td> healthConditions</td>
            <td> health-condition-events</td>
            <td>A collection of: Information about health events of the Animal </td>
</tr>
<tr>
            <td> calvings</td>
            <td> calving-events</td>
            <td>A collection of: Information about calvings of the Animal </td>
</tr>
<tr>
            <td> matings</td>
            <td> mating-events</td>
            <td>A collection of: Information about matings of the Animal </td>
</tr>
<tr>
            <td> heats</td>
            <td> heat-events</td>
            <td>A collection of: Information about health events of the Animal </td>
</tr>
<tr>
            <td> pregnancyDiagnoses</td>
            <td> pregnancy-diagnoses</td>
            <td> </td>
</tr>
<tr>
            <td> liveWeights</td>
            <td> live-weight-events</td>
            <td>A collection of: Information about live weigths recorded for the Animal </td>
</tr>
<tr>
            <td> eids</td>
            <td> electronic-id-events</td>
            <td>A collection of: Information about EIDs (electronic ids) of the Animal </td>
</tr>
<tr>
            <td> managementId</td>
            <td> management-id-events</td>
            <td>A collection of: Information about Management Ids of the Animal (deprecated) </td>
</tr>
<tr>
            <td> embryoImplants</td>
            <td> embryo-implant-events</td>
            <td>A collection of: Information about Embryo Implants of the Animal </td>
</tr>
<tr>
            <td> parentage.sire</td>
            <td> sire</td>
            <td> </td>
</tr>
<tr>
            <td> parentage.dam</td>
            <td> dam</td>
            <td> </td>
</tr>
<tr>
            <td> parentage.surrogateBirthDam</td>
            <td> recipient-dam</td>
            <td> </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/animal/2519150


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/animal/2519150"
      },
      {
         "rel": "herd-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/herd-event/"
      },
      {
         "rel": "in-milk-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/in-milk-event/"
      },
      {
         "rel": "health-condition-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/health-condition-event/"
      },
      {
         "rel": "calving-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/calving-event/"
      },
      {
         "rel": "mating-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/mating-event/"
      },
      {
         "rel": "heat-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/heat-event/"
      },
      {
         "rel": "pregnancy-diagnoses",
         "href": "http://www.example.com/animal-timeline/animal/2519150/pregnancy-diagnosis/"
      },
      {
         "rel": "live-weight-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/live-weight-event/"
      },
      {
         "rel": "electronic-id-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/electronic-id-event/"
      },
      {
         "rel": "management-id-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/management-id-event/"
      },
      {
         "rel": "embryo-implant-events",
         "href": "http://www.example.com/animal-timeline/animal/2519150/embryo-implant-event/"
      },
      {
         "rel": "sire",
         "href": "http://www.example.com/animal-timeline/animal/2519151"
      },
      {
         "rel": "dam",
         "href": "http://www.example.com/animal-timeline/animal/2519152"
      },
      {
         "rel": "donor-dam",
         "href": "http://www.example.com/animal-timeline/animal/2519153"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/animal-docs/"
      }
   ],
   "animalKey": 29866569,
   "dateOfInitialOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "birthDate": "2016-10-24T11:00:00.000000+00:00",
   "sex": "Female",
   "breeds": {
      "abbreviation": "JER",
      "portion16th": 16
   },
   "birthId": "HTRD-2017-1",
   "damOfficialStatus": "MatingConfimed",
   "sireOfficialStatus": "DNAConfirmed",
   "healthBoardId": {
      "ahbHerdNumber": 21,
      "year": 2008,
      "number": 5123
   }
}
```



# 3. Calving
        
The calving of an animal on some date.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>sequence</td>
                <td>integer</td>
                <td>The order of calves when twins, etc</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>calfSex</td>
                <td>string</td>
                <td>The sex of the calf.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>calfFate</td>
                <td>string</td>
                <td>The fate of the calf</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>pregnancyTermination</td>
                <td>string</td>
                <td>The type of pregnancy termination.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> calf</td>
            <td>The calf animal. </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/calving-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/calving-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/calving-event/"
      },
      {
         "rel": "calf",
         "href": "http://www.example.com/animal-timeline/animal/2417"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/calving-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "sequence": 1,
   "calfSex": "Female",
   "calfFate": "Weaned",
   "pregnancyTermination": "Normal"
}
```



# 4. ElectronicId
        
The EID of an animal over some time period.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>eid</td>
                <td>string</td>
                <td>The EID of the animal.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>isStart</td>
                <td>boolean</td>
                <td>If 'true', the dateOfOnFarmEvent is the start of the period. If 'false', the dateOfOnFarmEvent is the end of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfIdentificationStart</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The start date of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/electronic-id-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/electronic-id-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/electronic-id-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/electronic-id-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "eid": "982 000184935957",
   "isStart": true,
   "dateOfIdentificationStart": "2016-10-24T11:00:00.000000+00:00"
}
```



# 5. EmbryoImplant
        
The implant of an embryo in a recipient animal on some date.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The implant date.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>embryoTransferNumber</td>
                <td>string</td>
                <td>A unique number identifying the embryo transfer.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>comparableMatingDateTime</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The effective mating date i.e. implant date minus days embryo was in donor animal.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>inseminationDateTime</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of insemination.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>recoveryDateTime</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The embryo recovery date.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>inVitroProduction</td>
                <td>boolean</td>
                <td>'True' if the embryo was produced in vitro.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> donor-dam</td>
            <td>The donor animal. </td>
</tr>
<tr>
            <td> </td>
            <td> insemination-bull-animals</td>
            <td>The bull animal(s) used for insemination. </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/embryo-implant-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/embryo-implant-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/embryo-implant-event/"
      },
      {
         "rel": "donor-dam",
         "href": "http://www.example.com/animal-timeline/animal/42323/"
      },
      {
         "rel": "insemination-bull-animals",
         "href": "http://www.example.com/animal-timeline/animal/2415/embryo-implant-event/132/insemination-bull-animal"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/embryo-implant-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "embryoTransferNumber": 1231,
   "comparableMatingDateTime": "2016-10-24T11:00:00.000000+00:00",
   "inseminationDateTime": "2016-10-24T11:00:00.000000+00:00",
   "recoveryDateTime": "2016-10-24T11:00:00.000000+00:00",
   "inVitroProduction": "true"
}
```



# 6. GroupMembership
        
The entering or leaving of a herd by an animal on some date.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>enteredHerd</td>
                <td>boolean</td>
                <td>If 'true', the event is for the animal entering the herd. If 'false', the event is for the animal leaving the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfEntry</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the animal entered the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>fate</td>
                <td>string</td>
                <td>The fate of the animal when it left the herd.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/herd-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/herd-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/herd-event/"
      },
      {
         "rel": "animal",
         "href": "http://www.example.com/animal-timeline/animal/2415"
      },
      {
         "rel": "group",
         "href": "http://www.example.com/animal-timeline/group/555"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/herd-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2017-11-07T11:00:00.000000+00:00",
   "enteredHerd": false,
   "dateOfEntry": "2016-10-24T11:00:00.000000+00:00",
   "fate": "Sold"
}
```



# 7. AnimalHealthCondition
        
A health condition/treatment for an animal at some date.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>healthRecordId</td>
                <td>integer</td>
                <td>The legacy (Minda) id of the health record.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>conditionCategoryCode</td>
                <td>string</td>
                <td>The code for the health condition category.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>withholdingHours</td>
                <td>number</td>
                <td>The number of hours of the milk withholding period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dryCow</td>
                <td>boolean</td>
                <td>'True' if the cow is being dried off.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>withholdingHoursForMilk</td>
                <td>number</td>
                <td>The number of hours of the milk withholding period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>withholdingHoursForMeat</td>
                <td>number</td>
                <td>The number of hours of the meat withholding period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfDosage</td>
                <td>date</td>
                <td>Date of dosage.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>dosageValue</td>
                <td>number</td>
                <td>Amount of dosage.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>dosageCount</td>
                <td>number</td>
                <td>Count of dosage.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>dateOfReturnToVat</td>
                <td>date</td>
                <td>Date animals milk is used in vat again.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>meridiemOfReturnToVat</td>
                <td>string</td>
                <td>Meridiem of date when animals milk is used in vat again.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>affectedQuarters</td>
                <td>object</td>
                <td>Parts of the animal affected by health condition.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>veterinarian</td>
                <td>string</td>
                <td>Veterinarian name.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> condition</td>
            <td>Further information about the health condition. </td>
</tr>
<tr>
            <td> </td>
            <td> product</td>
            <td>Information about the health product used. </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/health-condition-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/health-condition-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/health-condition-event/"
      },
      {
         "rel": "condition",
         "href": "http://www.example.com/animal-timeline/condition/22"
      },
      {
         "rel": "product",
         "href": "http://www.example.com/animal-timeline/product/71"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/health-condition-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "healthRecordId": 23831613,
   "conditionCategoryCode": "INFC",
   "withholdingHours": 24,
   "dryCow": false,
   "withholdingHoursForMilk": 24,
   "withholdingHoursForMeat": 24,
   "dateOfDosage": "2017-05-30T23:40:40.326267+00:00",
   "dosageValue": 5.234,
   "dosageCount": 3,
   "dateOfReturnToVat": "2017-05-30T23:40:40.326267+00:00",
   "meridiemOfReturnToVat": "AM",
   "affectedQuarters": {
      "frontLeft": true,
      "frontRight": true,
      "rearLeft": true,
      "rearRight": true
   },
   "veterinarian": "Dr Susan Dolittle"
}
```



# 8. Heat
        
A heat event for an animal on some date.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/heat-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/heat-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/heat-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/heat-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00"
}
```



# 9. InMilk
        
The starting or ending of lactation or withholding by an animal.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>isStart</td>
                <td>boolean</td>
                <td>If 'true', the dateOfOnFarmEvent is the start of a period. if 'false', the dateOfOnFarmEvent is the end of a period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>isLactationEvent</td>
                <td>boolean</td>
                <td>If 'true', the event is a lactation event. if 'false', the event is a withholding event.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>reason</td>
                <td>string</td>
                <td>Whether the event is Lactation or Withholding.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>healthRecordId</td>
                <td>integer</td>
                <td>Used when it's a health record, so it can be deleted.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>dateOfLactationStart</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Used when it's a LactationEventIn, so it can be updated and deleted.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/in-milk-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/in-milk-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/in-milk-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/in-milk-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "isStart": true,
   "isLactationEvent": true,
   "reason": "LactationEventIn",
   "dateOfLactationStart": "2016-10-24T11:00:00.000000+00:00"
}
```



# 10. LiveWeight
        
The weight of an animal on some date (not yet loaded onto the cloud).


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>weight</td>
                <td>number</td>
                <td>The weight of the animal in kilograms.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/live-weight-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/live-weight-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/live-weight-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/live-weight-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "weight": 460
}
```



# 11. ElectronicId
        
The EID of an animal over some time period.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>eid</td>
                <td>string</td>
                <td>The EID of the animal.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>isStart</td>
                <td>boolean</td>
                <td>If 'true', the dateOfOnFarmEvent is the start of the period. If 'false', the dateOfOnFarmEvent is the end of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfIdentificationStart</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The start date of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/electronic-id-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/electronic-id-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/electronic-id-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/electronic-id-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "eid": "982 000184935957",
   "isStart": true,
   "dateOfIdentificationStart": "2016-10-24T11:00:00.000000+00:00"
}
```



# 12. ManagementId  (deprecated)
        
The Management ID of an animal over some time period, stored as one or two records.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>managementNumber</td>
                <td>number</td>
                <td>The Management ID of the animal.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>isStart</td>
                <td>boolean</td>
                <td>If 'true', the dateOfOnFarmEvent is the start of the period. If 'false', the dateOfOnFarmEvent is the end of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfIdentificationStart</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The start date of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/management-id-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/management-id-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/management-id-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/management-id-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "managementNumber": 451,
   "isStart": true,
   "dateOfIdentificationStart": "2016-10-24T11:00:00.000000+00:00"
}
```



# 13. ManagementId
        
The Management ID of an animal over some time period.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>startDate</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The start date of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>endDate</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The end date of the period.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>managementNumber</td>
                <td>number</td>
                <td>The Management ID of the animal.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/management-id-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/management-id-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/management-id-event/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/management-id-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "startDate": "2016-10-24T11:00:00.000000+00:00",
   "endDate": "2017-11-07T11:00:00.000000+00:00",
   "managementNumber": 451
}
```



# 14. Mating
        
The mating of an animal on some date


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>matingType</td>
                <td>string</td>
                <td>The type of mating.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>mateChargeType</td>
                <td>string</td>
                <td>The charge type.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>coreProductCode</td>
                <td>string</td>
                <td>The core product code.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> sire</td>
            <td>The sire animal. </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/mating-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/mating-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/mating-event/"
      },
      {
         "rel": "sire",
         "href": "http://www.example.com/animal-timeline/animal/2416"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/mating-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "matingType": "OtherAi",
   "mateChargeType": "Premier Sires",
   "coreProductCode": "SGL"
}
```



# 15. GroupMembership
        
The group membership of an animal over some time period.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>startDate</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The start date of the period.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>endDate</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The end date of the period.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>fate</td>
                <td>string</td>
                <td>The fate of the animal when it left the herd.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/herd-event/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/herd-event/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/herd-event/"
      },
      {
         "rel": "animal",
         "href": "http://www.example.com/animal-timeline/animal/2415"
      },
      {
         "rel": "group",
         "href": "http://www.example.com/animal-timeline/group/555"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/herd-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "startDate": "2016-10-24T11:00:00.000000+00:00",
   "endDate": "2016-10-24T11:00:00.000000+00:00",
   "fate": "Sold"
}
```



# 16. PregnancyDiagnosis
        
A pregnancy diagnosis event for an animal.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date the event was created in the system.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The date of the event on the farm.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>pregnancyStatus</td>
                <td>string</td>
                <td>The pregnancy diagnosis.</td>
                <td>Empty, Pregnant, Doubtful</td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>daysPregnant</td>
                <td>number</td>
                <td>The number of days the cow has been pregnant</td>
                <td>Must be between 21 and 302. Must only be provided if the pregnancyStatus is 'Pregnant'.</td>
                <td class="boolean">&#10003;</td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/pregnancy-diagnosis/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/pregnancy-diagnosis/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/animal/2415/pregnancy-diagnosis/"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/pregnancy-diagnosis-event-docs/"
      }
   ],
   "dateOfEventCreation": "2017-05-30T23:40:40.326267+00:00",
   "dateOfOnFarmEvent": "2016-10-24T11:00:00.000000+00:00",
   "pregnancyStatus": "Pregnant",
   "daysPregnant": 55
}
```



<h3>POST</h3>
http://www.example.com/animal-timeline/animal/2415/pregnancy-diagnosis

<h4>Request</h4>

```json
{
   "animalId": 2415,
   "observationDate": "2016-10-24T11:00:00.000000+00:00",
   "pregnancyStatus": "Pregnant",
   "daysPregnant": 55
}
```




# 17. Group
        
Group: a Herd that contains Animals at different times


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>participantCode</td>
                <td><a href="/animal-timeline/docs/participant-code-docs/">participantCode</a></td>
                <td>The current participant code.</td>
                <td>4 upper-case consonant letters, such as 'NTFG'</td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>name</td>
                <td>string</td>
                <td>The Group (herd) name.</td>
                <td>Can not be empty string.</td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>animalGroupId</td>
                <td>string</td>
                <td>The primary Minda legacy key for a Group (herd).</td>
                <td>The string seems to always hold a positive integer.</td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateOfInitialOnFarmEvent</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>The earliest date that the Group was referred to.</td>
                <td></td>
                <td class="boolean">&#10003;</td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> currentAnimals.animalsInGroupUri</td>
            <td> animals</td>
            <td>A collection of: Animal currently in Group </td>
</tr>
<tr>
            <td> currentAnimals.animalsInGroupPaginatedUri</td>
            <td> animals-paginated</td>
            <td>A collection of: Animal currently in Group </td>
</tr>
<tr>
            <td> groupAggregationByDay.animalCounts.feedUri</td>
            <td> animal-counts-by-days</td>
            <td>A collection of: For each day (where it differs from previous):  A count of the number of animals in the herd, plus those with management numbers. </td>
</tr>
<tr>
            <td> groupAggregationByDay.animalCounts.resourceUri</td>
            <td> animal-counts-by-day</td>
            <td>For each day (where it differs from previous):  A count of the number of animals in the herd, plus those with management numbers. </td>
</tr>
<tr>
            <td> groupAggregationByDay.breedComposition.feedUri</td>
            <td> breed-composition-by-days</td>
            <td>A collection of: For each day (where it differs from previous):  An average of the breeds of the animals in a herd (only of animals of age with a management number). </td>
</tr>
<tr>
            <td> groupAggregationByDay.breedComposition.resourceUri</td>
            <td> breed-composition-by-day</td>
            <td>For each day (where it differs from previous):  An average of the breeds of the animals in a herd (only of animals of age with a management number). </td>
</tr>
<tr>
            <td> groupAggregationByDay.inVat.feedUri</td>
            <td> in-vat-by-days</td>
            <td>A collection of: For each day (where it differs from previous):  A count of the number of lactating animals and those supplying milk to the vat (only of animals of age with a management number). </td>
</tr>
<tr>
            <td> groupAggregationByDay.inVat.resourceUri</td>
            <td> in-vat-by-day</td>
            <td>For each day (where it differs from previous):  A count of the number of lactating animals and those supplying milk to the vat (only of animals of age with a management number). </td>
</tr>
<tr>
            <td> groupAggregationByDay.animalIndex.feedUri</td>
            <td> animal-index-by-days</td>
            <td>A collection of: For each day (where it differs from previous):  An average of the breeds of the animals in a herd (only of animals of age with a management number). </td>
</tr>
<tr>
            <td> groupAggregationByDay.animalIndex.resourceUri</td>
            <td> group-animal-index-by-day</td>
            <td>For each day (where it differs from previous):  An average of the breeds of the animals in a herd (only of animals of age with a management number). </td>
</tr>
<tr>
            <td> groupAggregationByDay.cowsCalved.feedUri</td>
            <td> cows-calved-by-days</td>
            <td>A collection of: A count of the dams that have calved on a day </td>
</tr>
<tr>
            <td> groupAggregationByDay.cowsCalved.resourceUri</td>
            <td> group-cows-calved-by-day</td>
            <td>A count of the dams that have calved on a day </td>
</tr>
<tr>
            <td> place</td>
            <td> place</td>
            <td>The Group's Place </td>
</tr>
<tr>
            <td> herdTestResults</td>
            <td> herd-test-results</td>
            <td>A collection of: Herd Test Result </td>
</tr>
<tr>
            <td> birthIdReservationUris.reservationResourceUri</td>
            <td> birth-id-reservation</td>
            <td>An existing Birth Id Reservation </td>
</tr>
<tr>
            <td> managementNumberReservationUris.reservationResourceUri</td>
            <td> management-number-reservation</td>
            <td>An existing Management Number Reservation </td>
</tr>
<tr>
            <td> managementNumbersCsv</td>
            <td> management-numbers-csv</td>
            <td>Currently-used Management Numbers in the Group </td>
</tr>
<tr>
            <td> reconciliations</td>
            <td> reconciliation-group</td>
            <td>Reconciliation Details for the Group </td>
</tr>
</table>


<h3>Links to Forms</h3>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Form Parameters</th>
                <th>Results</th>
</tr>   

        <tr>
            <td> currentAnimals.searchFormUri</td>
            <td> search-for-current-animal</td>
            <td><table><tr>
                <td>animalKey</td>
                <td>number</td>
                <td>AnimalKey of the animal of interest</td>
            </tr></table></td>
            <td>Animal</td>
        </tr>

        <tr>
            <td> herdHealth</td>
            <td> herd-health-report</td>
            <td><table><tr>
                <td>dateFrom</td>
                <td>UTC date string</td>
                <td>starting date of Herd Health report</td>
            </tr>
<tr>
                <td>dateTo</td>
                <td>UTC date string</td>
                <td>ending date of Herd Health report</td>
            </tr></table></td>
            <td>The Herd Health Report</td>
        </tr>

        <tr>
            <td> birthIdReservationUris.queryUri</td>
            <td> birth-id-query</td>
            <td><table><tr>
                <td>allocationYear</td>
                <td>number</td>
                <td>Year of BirthIds</td>
            </tr>
<tr>
                <td>quantity</td>
                <td>number</td>
                <td>Number of BirthIds</td>
            </tr>
<tr>
                <td>startNumber</td>
                <td>number</td>
                <td>First number of the range</td>
            </tr>
<tr>
                <td>ranges</td>
                <td>string</td>
                <td>Preferred number ranges for BirthIds</td>
            </tr></table></td>
            <td>Birth Id Ranges Available</td>
        </tr>

        <tr>
            <td> birthIdReservationUris.reservationUri</td>
            <td> birth-id-reservation</td>
            <td><table><tr>
                <td>requestID</td>
                <td>string</td>
                <td>Unique ID for request, to allow it to be idempotent</td>
            </tr>
<tr>
                <td>allocationYear</td>
                <td>number</td>
                <td>Year of BirthIds</td>
            </tr>
<tr>
                <td>ranges</td>
                <td>string</td>
                <td>Preferred number ranges for BirthIds</td>
            </tr>
<tr>
                <td>allocationParties</td>
                <td>string</td>
                <td>JSON string giving details of the parties involved in the request</td>
            </tr></table></td>
            <td>Birth Id Reservation</td>
        </tr>

        <tr>
            <td> birthIdReservationUris.allocateUri</td>
            <td> allocate</td>
            <td><table></table></td>
            <td>Birth Id Allocation</td>
        </tr>

        <tr>
            <td> birthIdReservationUris.cancelUri</td>
            <td> cancel</td>
            <td><table></table></td>
            <td>Cancelled BirthId Reservation</td>
        </tr>

        <tr>
            <td> birthIdReservationUris.availableRangesUri</td>
            <td> available</td>
            <td><table><tr>
                <td>allocationYear</td>
                <td>number</td>
                <td>The year of allocation that is of interest</td>
            </tr></table></td>
            <td>Available BirthId ranges</td>
        </tr>

        <tr>
            <td> managementNumberReservationUris.queryUri22</td>
            <td> management-number-query</td>
            <td><table><tr>
                <td>quantity</td>
                <td>number</td>
                <td>Number of management numbers</td>
            </tr>
<tr>
                <td>startNumber</td>
                <td>number</td>
                <td>First number of the range</td>
            </tr>
<tr>
                <td>ranges</td>
                <td>string</td>
                <td>Preferred number ranges for management numbers</td>
            </tr></table></td>
            <td>Management Numbers</td>
        </tr>

        <tr>
            <td> managementNumberReservationUris.quantityQueryUri</td>
            <td> management-number-quantity-query</td>
            <td><table><tr>
                <td>quantity</td>
                <td>number</td>
                <td>Number of management numbers</td>
            </tr>
<tr>
                <td>startNumber</td>
                <td>number</td>
                <td>First number of the range</td>
            </tr>
<tr>
                <td>states</td>
                <td>Array of string</td>
                <td>States used to filter management numbers returned</td>
            </tr></table></td>
            <td>Management Numbers</td>
        </tr>

        <tr>
            <td> managementNumberReservationUris.rangeQueryUri</td>
            <td> management-number-range-query</td>
            <td><table><tr>
                <td>requestID</td>
                <td>string</td>
                <td>Unique ID for request, to allow it to be idempotent</td>
            </tr>
<tr>
                <td>ranges</td>
                <td>string</td>
                <td>Preferred number ranges for management numbers</td>
            </tr></table></td>
            <td>Management Number Reservation</td>
        </tr>

        <tr>
            <td> managementNumberReservationUris.reservationUri</td>
            <td> management-number-reservation</td>
            <td><table><tr>
                <td>requestID</td>
                <td>string</td>
                <td>Unique ID for request, to allow it to be idempotent</td>
            </tr>
<tr>
                <td>ranges</td>
                <td>string</td>
                <td>Preferred number ranges for management numbers</td>
            </tr></table></td>
            <td>Management Number Reservation</td>
        </tr>

        <tr>
            <td> managementNumberReservationUris.confirmUri</td>
            <td> confirm</td>
            <td><table></table></td>
            <td>Management Number Reservation</td>
        </tr>

        <tr>
            <td> managementNumberReservationUris.cancelUri</td>
            <td> cancel</td>
            <td><table></table></td>
            <td>Management number reservation</td>
        </tr>
</table>






<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/group/5395


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/group/5395"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/group/"
      },
      {
         "rel": "animals",
         "href": "http://www.example.com/animal-timeline/group/5395/animal"
      },
      {
         "rel": "search-for-current-animal",
         "href": "http://www.example.com/animal-timeline/group/5395/animal/search"
      },
      {
         "rel": "herd-health-report",
         "href": "http://www.example.com/animal-timeline/group/5395/herd-health-report"
      },
      {
         "rel": "animal-counts-by-days",
         "href": "http://www.example.com/animal-timeline/group/5395/animal-counts-by-day"
      },
      {
         "rel": "breed-composition-by-days",
         "href": "http://www.example.com/animal-timeline/group/5395/breed-composition-by-day"
      },
      {
         "rel": "in-vat-by-days",
         "href": "http://www.example.com/animal-timeline/group/5395/in-vat-by-day"
      },
      {
         "rel": "animal-index-by-days",
         "href": "http://www.example.com/animal-timeline/group/5395/animal-index-by-day"
      },
      {
         "rel": "place",
         "href": "http://www.example.com/animal-timeline/group/5395/place"
      },
      {
         "rel": "herd-test-results",
         "href": "http://www.example.com/animal-group/group/5395/herd-test-results"
      },
      {
         "rel": "request-birth-identifications",
         "href": "http://www.example.com/animal-timeline/group/5395/request-birth-identifications"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/group/"
      }
   ],
   "animalGroupId": "5000000",
   "name": "Jerseys",
   "participantCode": "BNKW",
   "dateOfInitialOnFarmEvent": "2016-10-24T11:00:00.000000+00:00"
}
```



# 18. GroupCountsByDay
        
Counts of animals in the herd, and counts of animals in the herd that are at least 490 days old and have a Management Id.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>day</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Day of changed counts.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>totalAnimalsInGroup</td>
                <td>integer</td>
                <td>Count of animals in the herd on that day.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>totalOfAge</td>
                <td>integer</td>
                <td>Count of animals in the herd on that day that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/animal-counts-by-day/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/animal-counts-by-day/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/group/241/animal-counts-by-day"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/group/animal-counts-by-day-docs"
      }
   ],
   "day": "2017-05-30T23:40:40.326267+00:00",
   "totalAnimalsInGroup": 73,
   "totalOfAge": 67
}
```



# 19. GroupAnimalIndexByDay
        
Total indexes across the herd for animals that are at least 490 days old and have a Management Id.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>day</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Day of changed animal indexes.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>breedingWorth</td>
                <td>number</td>
                <td>Sum of breeding worth indexes for animals in the herd that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>breedingWorthReliability</td>
                <td>number</td>
                <td>Average reliability of breeding worth indexes across the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>productionWorth</td>
                <td>number</td>
                <td>Sum of production worth indexes for animals in the herd that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>productionWorthReliability</td>
                <td>number</td>
                <td>Average reliability of production worth indexes across the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>animalCount</td>
                <td>number</td>
                <td>Count of animals in the herd that have an animal index, are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>lactationWorth</td>
                <td>number</td>
                <td>Sum of lactation worth indexes for animals in the herd that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>lactationWorthCount</td>
                <td>number</td>
                <td>Count of animals in the herd that have a lactation worth index, are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightBreedWorth</td>
                <td>number</td>
                <td>Sum of live weight breed worth indexes for animals in the herd that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightBreedWorthReliability</td>
                <td>number</td>
                <td>Average reliability of live weight breeding worth indexes across the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightProductionWorth</td>
                <td>number</td>
                <td>Sum of live weight production worth indexes for animals in the herd that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightProductionWorthReliability</td>
                <td>number</td>
                <td>Average reliability of live weight production worth indexes across the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightAnimalCount</td>
                <td>number</td>
                <td>Count of animals in the herd that have a live weight index, are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightLactationWorth</td>
                <td>number</td>
                <td>Sum of live weight lactation worth indexes for animals in the herd that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>liveWeightLactationWorthCount</td>
                <td>number</td>
                <td>Count of animals in the herd that have a live weight lactation worth index, are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/animal-index-by-day/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/animal-index-by-day/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/group/241/animal-index-by-day"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/group/animal-index-by-day-docs"
      }
   ],
   "day": "2017-05-30T23:40:40.326267+00:00",
   "breedingWorth": 542,
   "breedingWorthReliability": 67,
   "productionWorth": 42,
   "productionWorthReliability": 32,
   "animalCount": 67,
   "lactationWorth": -33,
   "lactationWorthCount": 83,
   "liveWeightBreedWorth": 332,
   "liveWeightBreedWorthReliability": 3,
   "liveWeightProductionWorth": 3777,
   "liveWeightProductionWorthReliability": 83,
   "liveWeightAnimalCount": 55,
   "liveWeightLactationWorth": 254,
   "liveWeightLactationWorthCount": 42
}
```



# 20. GroupBreedCompositionByDay
        
Breed composition across the herd for animals that are at least 490 days old and have a Management Id.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>day</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Day of changed breed composition.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>breedCounts</td>
                <td><a href="/animal-timeline/docs/animal-breed-count-docs">AnimalBreedCounts</a></td>
                <td>For every different breed that occurs within the herd, specify the breed, the total 16ths and the number of animals with that breed. This only applies to animals that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/breed-composition-by-day/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/breed-composition-by-day/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/group/241/breed-composition-by-day"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/group/breed-composition-by-day-docs"
      }
   ],
   "day": "2017-05-30T23:40:40.326267+00:00",
   "breedCounts": [
      {
         "breed": "JER",
         "portion16th": 1072,
         "count": 67
      }
   ]
}
```



# 21. GroupCowsCalvedByDay
        
Count of animals in the herd that have calved on a day.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>day</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Day of changed counts.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>totalCowsCalved</td>
                <td>integer</td>
                <td>Count of animals in the herd that have calved on that day.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/cows-calved-by-day/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/cows-calved-by-day/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/group/241/cows-calved-by-day"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/group/cows-calved-by-day-docs"
      }
   ],
   "day": "2017-05-30T23:40:40.326267+00:00",
   "totalCowsCalved": 14
}
```



# 22. GroupInVatByDay
        
Counts of animals in the herd that are lactating, and those that have milk going to the vat. This only applies to animals that are at least 490 days old and have a Management Id.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>day</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Day of changes to animals lactating and in vat.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>totalLactatingAnimals</td>
                <td>integer</td>
                <td>Count of animals in the herd that are lactating on that day, that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>totalAnimalsInVat</td>
                <td>integer</td>
                <td>Count of animals in the herd that have milk going to the vat on that day, that are at least 490 days old and have a Management Id.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>











<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/in-vat-by-day/132


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/in-vat-by-day/132"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/group/241/in-vat-by-day"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/group/in-vat-by-day-docs"
      }
   ],
   "day": "2017-05-30T23:40:40.326267+00:00",
   "totalLactatingAnimals": 73,
   "totalAnimalsInVat": 67
}
```



# 23. PublishGroupAggregate
        
Summary of which group-aggregated values have changed within a certain date range. For daily events, the date range will be over one day. For events from the past, the date range will be over multiple days.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>dateOfEventCreation</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Date of publication</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateFrom</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>Start of date range for summary</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>dateUpTo</td>
                <td><a href="/animal-timeline/docs/utc-string-docs/">UTC string</a></td>
                <td>End of date range for summary</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>animalsCountsChanged</td>
                <td>boolean</td>
                <td>Whether animal counts in herd have changed within the date range</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>animalsCowsCalvedChanged</td>
                <td>boolean</td>
                <td>Whether counts of cows that have calved in the herd have changed within the date range</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>animalsBreedCompositionChanged</td>
                <td>boolean</td>
                <td>Whether breed composition of herd has changed within the date range</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>animalsIndexChanged</td>
                <td>boolean</td>
                <td>Whether animal index values of herd have changed within the date range</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>animalsInVatChanged</td>
                <td>boolean</td>
                <td>Whether counts of lactating or in-vat animals in the herd have changed within the date range</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> group</td>
            <td>The Group for this PublishGroupAggregate </td>
</tr>
<tr>
            <td> </td>
            <td> group-aggregates-report</td>
            <td>A report of all changes to the Group for this PublishGroupAggregate </td>
</tr>
</table>









# 24. HealthCondition
        
A health condition code and description


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>code</td>
                <td>string</td>
                <td>2-letter condition code</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>description</td>
                <td>string</td>
                <td>Description of the condition</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> condition-category</td>
            <td>The category of the condition </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/condition/22


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/condition/22"
      },
      {
         "rel": "condition-category",
         "href": "http://www.example.com/animal-timeline/condition-category/12"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/condition/"
      }
   ],
   "code": "CC",
   "description": "Coccidiosis"
}
```



# 25. HealthConditionCategory
        
A health condition category code and description


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>code</td>
                <td>string</td>
                <td>4-letter category code</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>description</td>
                <td>string</td>
                <td>Description of the category</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> conditions</td>
            <td>A list of the health conditions in this category </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/condition-category/12


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/condition-category/12"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/condition-category/"
      },
      {
         "rel": "conditions",
         "href": "http://www.example.com/animal-timeline/condition-category/12/condition"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/condition-category/"
      }
   ],
   "code": "INFC",
   "description": "INFECTIOUS DISEASES"
}
```



# 26. HealthProduct
        
A health product code and description


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>code</td>
                <td>string</td>
                <td>A product code</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>description</td>
                <td>string</td>
                <td>Description of the product</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> product-category</td>
            <td>The category of the product </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/product/71


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/product/71"
      },
      {
         "rel": "product-category",
         "href": "http://www.example.com/animal-timeline/product-category/14"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/product/"
      }
   ],
   "code": "00000",
   "description": "Trimming of Hoof"
}
```



# 27. HealthProductCategory
        
A health product category code and description


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>code</td>
                <td>string</td>
                <td>4-letter category code</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>description</td>
                <td>string</td>
                <td>Description of the category</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>



<h2>Links</h2>
<p>Visibility of these links may depend on the user.</p>
<table>
<tr>
                <th>Context</th>
                <th>Link title</th>
                <th>Description</th>
</tr>   

<tr>
            <td> </td>
            <td> products</td>
            <td>A list of the health products in this category </td>
</tr>
</table>








<h3>Examples</h3>

<h3>GET</h3>
http://www.example.com/animal-timeline/product-category/14


<h4>Response</h4>

```json
{
   "links": [
      {
         "rel": "self",
         "href": "http://www.example.com/animal-timeline/product-category/14"
      },
      {
         "rel": "up",
         "href": "http://www.example.com/animal-timeline/product-category/"
      },
      {
         "rel": "products",
         "href": "http://www.example.com/animal-timeline/product-category/14/product"
      },
      {
         "rel": "docs",
         "href": "http://www.example.com/animal-timeline/docs/product-category/"
      }
   ],
   "code": "MISC",
   "description": "MISCELLANEOUS"
}
```



# 28. AHBIdentifier
        
The Animal Health Board ID.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>ahbHerdNumber</td>
                <td>number</td>
                <td>The Animal Health Board herd number.</td>
                <td>7-digit integer</td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>year</td>
                <td>number</td>
                <td>The year of the ID.</td>
                <td>2 digits e.g. '12' for year 2012</td>
                <td class="boolean">&#10003;</td>
</tr>

<tr>
                <td>number</td>
                <td>number</td>
                <td>The number of the animal within the year.</td>
                <td>4-digit integer</td>
                <td class="boolean"></td>
</tr>
</table>












# 29. AnimalBreedCounts
        
A summary of the breed portions of the animals in the herd


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>breed</td>
                <td>string</td>
                <td>A 3-letter abbreviation for the breed.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>portion16ths</td>
                <td>number</td>
                <td>The total number of 16th portions of this breed for the 'of age' animals in the herd.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>count</td>
                <td>number</td>
                <td>The number of animals included in the portion16ths.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>












# 30. AnimalBreed
        
A summary of the breed portions of the animal


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>abbreviation</td>
                <td>string</td>
                <td>A 3-letter abbreviation for the breed.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>portion16ths</td>
                <td>number</td>
                <td>The number of 16th portions of this breed for the animal.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>












# 31. BirthIdentifier
        
An identifier consisting of a prefix, year and sequence, separated by hyphens. For example: HTRD-2017-1.


<h3>Attributes</h3>
<table>
<tr>
                    <th>Attribute</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Constraints</th>
                    <th>Optional</th>
</tr>

<tr>
                <td>prefix</td>
                <td><a href="/animal-timeline/docs/participant-code-docs/">participantCode</a></td>
                <td>A legacy MINDA identifier for an organisation.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>year</td>
                <td>number</td>
                <td>The birth year.</td>
                <td></td>
                <td class="boolean"></td>
</tr>

<tr>
                <td>sequence</td>
                <td>number</td>
                <td>The calving sequence.</td>
                <td></td>
                <td class="boolean"></td>
</tr>
</table>












# 32. ParticipantCode
        
String consisting of 4 characters (all consonants). A legacy MINDA identifier for an organisation.













# 33. TransactionState
        
The state of the transaction.










<h3>Possible values</h3>
<p>- Pending</p><p>- Completed</p><p>- Failed</p>



# 34. UTC string
        
A date string in UTC format. For example: 2016-05-01T12:51:23.000000+00:00













