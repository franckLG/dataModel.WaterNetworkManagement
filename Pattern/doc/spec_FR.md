Entité : Modèle  
===============







- `id`  

<details><summary><strong>full yaml details</strong></summary>    

Pattern:    
  description: 'This entity contains a harmonised description of a generic pattern made for the Water Network Management domain. This entity is primarily associated with the water management vertical and related IoT applications.'    
  properties:    
    description:    
      description: 'An optional text that describes other significant information about the junction'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    multipliers:    
      description: 'Multipliers define how some base quantity (e.g., demand) is adjusted for each time period'    
      items:    
        type: number    
      type: Property    
    startTime:    
      description: 'The time at which the pattern starts'    
      format: date-time    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Time    
    tag:    
      description: 'An optional text string used to assign the pipe to a category, perhaps one based on age or material'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    timeStep:    
      description: 'The time step used for the multipliers. All units are accepted in [CEFACT](https://www.unece.org/cefact.html) code.'    
      format: date-time    
      type: Property    
      x-ngsi:    
        units: Second    
    type:    
      description: 'NGSI-LD Entity Type. It has to be Pattern'    
      enum:    
        - Pattern    
      type: Property    
  required:    
    - id    
    - type    
    - multipliers    
    - timeStep    
    - startTime    
  type: object    
```  
</details>    





    "id": "fbcb5fc8-8ca3-4533-a2eb-34bc89262190",  
    "type": "Pattern",  
    "multipliers": [  
        0.5692,  
        0.4647,  
        0.4385,  
        0.3604,  
        0.3098,  
        0.3345  
    ],  
    "timeStep": 3600,  
    "description": "Open Text",  
    "tag": "DMA1"  
}  
```  




    "id": "fbcb5fc8-8ca3-4533-a2eb-34bc89262190",  
    "type": "Pattern",  
    "multipliers": {  
        "value": [  
            0.5692,  
            0.4647,  
            0.4385,  
            0.3604,  
            0.3098,  
            0.3345  
        ]  
    },  
    "timeStep": {  
        "value": 3600  
    },  
    "description": {  
        "value": "Open Text"  
    },  
    "tag": {  
        "value": "DMA1"  
    }  
}  
```  




 "createdAt": "2020-02-20T17:43:00Z",  
 "description": "Open Text",  
 "id": "urn:ngsi-ld:Pattern:fbcb5fc8-8ca3-4533-a2eb-34bc89262190",  
 "modifiedAt": "2020-02-20T17:43:00Z",  
 "multipliers": [0.5692, 0.4647, 0.4385, 0.3604, 0.3098, 0.3345],  
 "startTime": "00:00",  
 "tag": "DMA1",  
 "timeStep": 3600,  
 "type": "Pattern"}  
```  




    "id": "urn:ngsi-ld:Pattern:fbcb5fc8-8ca3-4533-a2eb-34bc89262190",  
    "type": "Pattern",  
    "createdAt": "2020-02-20T17:43:00Z",  
    "modifiedAt": "2020-02-20T17:43:00Z",  
    "multipliers": {  
        "type": "Property",  
        "value": [0.5692, 0.4647, 0.4385, 0.3604, 0.3098, 0.3345],  
        "unitCode":"C62"  
    },  
    "timeStep": {  
        "type": "Property",  
        "value": 3600,  
        "unitCode": "SEC"  
    },  
    "description": {  
        "type": "Property",  
        "value": "Open Text"  
    },  
    "startTime": {  
        "type": "Property",  
        "value": "00:00"  
    },  
    "tag": {  
        "type": "Property",  
        "value": "DMA1"  
    },  
    "@context": [  
        "https://schema.lab.fiware.org/ld/context"  
    ]  
}  
```  