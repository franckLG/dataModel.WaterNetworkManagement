Entity: Pipe  
============







```yaml  
Pipe:    
  description: 'This entity contains a harmonised description of a generic pipe made for the Water Network Management domain. This entity is primarily associated with the water management vertical and related IoT applications.'    
  properties:    
    bulkCoeff:    
      properties: &pipe_-_properties_-_diameter_-_properties    
        createdAt:    
          format: date-time    
          type: string    
        modifiedAt:    
          format: date-time    
          type: string    
        observedAt:    
          format: date-time    
          type: string    
        type:    
          enum:    
            - Property    
          type: string    
        unitCode:    
          type: string    
        value:    
          type:    
            - number    
            - string    
            - array    
      required: &pipe_-_properties_-_diameter_-_required    
        - type    
        - value    
      type: object    
    diameter:    
      properties: *pipe_-_properties_-_diameter_-_properties    
      required: *pipe_-_properties_-_diameter_-_required    
      type: object    
    endsAt:    
      properties: &pipe_-_properties_-_startsat_-_properties    
        createdAt:    
          format: date-time    
          type: string    
        modifiedAt:    
          format: date-time    
          type: string    
        object:    
          format: uri    
          type:    
            - string    
        observedAt:    
          format: date-time    
          type: string    
        type:    
          enum:    
            - Relationship    
          type: string    
      required: &pipe_-_properties_-_startsat_-_required    
        - type    
        - object    
      type: object    
    initialStatus:    
      properties: &pipe_-_properties_-_status_-_properties    
        observedAt:    
          format: date-time    
          type: string    
        type:    
          enum:    
            - Property    
          type: string    
        unitCode:    
          type: string    
        value:    
          enum:    
            - OPEN    
            - CLOSED    
            - CV    
          type:    
            - number    
            - string    
            - array    
      required: &pipe_-_properties_-_status_-_required    
        - type    
        - value    
      type: object    
    length:    
      properties: *pipe_-_properties_-_diameter_-_properties    
      required: *pipe_-_properties_-_diameter_-_required    
      type: object    
    minorLoss:    
      properties: *pipe_-_properties_-_diameter_-_properties    
      required: *pipe_-_properties_-_diameter_-_required    
      type: object    
    roughness:    
      properties: *pipe_-_properties_-_diameter_-_properties    
      required: *pipe_-_properties_-_diameter_-_required    
      type: object    
    startsAt:    
      properties: *pipe_-_properties_-_startsat_-_properties    
      required: *pipe_-_properties_-_startsat_-_required    
      type: object    
    status:    
      properties: *pipe_-_properties_-_status_-_properties    
      required: *pipe_-_properties_-_status_-_required    
      type: object    
    tag:    
      properties: *pipe_-_properties_-_diameter_-_properties    
      required: *pipe_-_properties_-_diameter_-_required    
      type: object    
    type:    
      description: 'NGSI-LD Entity Type'    
      enum:    
        - Pipe    
      type: string    
    vertices:    
      oneOf:    
        - $id: https://geojson.org/schema/MultiPoint.json    
          $schema: "http://json-schema.org/draft-07/schema#"    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPoint'    
          type: object    
        - $id: https://geojson.org/schema/Point.json    
          $schema: "http://json-schema.org/draft-07/schema#"    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Point'    
          type: object    
    wallCoeff:    
      properties: *pipe_-_properties_-_diameter_-_properties    
      required: *pipe_-_properties_-_diameter_-_required    
      type: object    
  required:    
    - id    
    - type    
    - initialStatus    
    - length    
    - diameter    
    - roughness    
    - minorLoss    
    - startsAt    
    - endsAt    
  type: object    
```  



    "id": "74azsty-70d4l-4da9-b7d0-3340ef655nnb",  
    "type": "Pipe",  
    "initialStatus": "OPEN",  
    "status": "OPEN",  
    "length": 52.90,  
    "diameter": 203.00,  
    "roughness": 72.4549,  
    "minorLoss": 72.4549,  
    "tag": "DMA1",  
    "description": "Free Text",  
    "startsAt": "63fe7d79-0d4c-4da9-b7d0-3340efa0656a",  
    "endsAt": "1863179e-3768-4480-9167-ff21f870dd19",  
    "bulkCoeff": 72.4549,  
    "wallCoeff": 72.4549  
}  
```  



    "id": "74azsty-70d4l-4da9-b7d0-3340ef655nnb",  
    "type": "Pipe",  
    "initialStatus": {  
        "value": "OPEN"  
    },  
    "status": {  
        "value": "OPEN"  
    },  
    "length": {  
        "value": 52.90  
    },  
    "diameter": {  
        "value": 203.00  
    },  
    "roughness": {  
        "value": 72.4549  
    },  
    "minorLoss": {  
        "value": 72.4549  
    },  
    "tag": {  
        "value": "DMA1"  
    },  
    "description": {  
        "value": "Free Text"  
    },  
    "startsAt": {  
        "type": "Relationship",  
        "value": "63fe7d79-0d4c-4da9-b7d0-3340efa0656a"  
    },  
    "endsAt": {  
        "type": "Relationship",  
        "value": "1863179e-3768-4480-9167-ff21f870dd19"  
    },  
    "bulkCoeff": {  
        "value": 72.4549  
    },  
    "wallCoeff": {  
        "value": 72.4549  
    }  
}  
```  



 "bulkCoeff": 72.4549,  
 "createdAt": "2020-02-20T15:42:00Z",  
 "description": "Free Text",  
 "diameter": 203.0,  
 "endsAt": "urn:ngsi-ld:Reservoir:1863179e-3768-4480-9167-ff21f870dd19",  
 "id": "urn:ngsi-ld:Pipe:74azsty-70d4l-4da9-b7d0-3340ef655nnb",  
 "initialStatus": "OPEN",  
 "length": 52.9,  
 "minorLoss": 72.4549,  
 "modifiedAt": "2020-02-20T15:45:00Z",  
 "roughness": 72.4549,  
 "startsAt": "urn:ngsi-ld:Junction:63fe7d79-0d4c-4da9-b7d0-3340efa0656a",  
 "status": "OPEN",  
 "tag": "DMA1",  
 "type": "Pipe",  
 "wallCoeff": 72.4549}  
```  



    "id": "urn:ngsi-ld:Pipe:74azsty-70d4l-4da9-b7d0-3340ef655nnb",  
    "type": "Pipe",  
    "createdAt": "2020-02-20T15:42:00Z",  
    "modifiedAt": "2020-02-20T15:45:00Z",  
    "initialStatus": {  
        "type": "Property",  
        "value": "OPEN"  
    },  
    "status": {  
        "type": "Property",  
        "value": "OPEN"  
    },  
    "length": {  
        "type": "Property",  
        "value": 52.90,  
        "unitCode": "MTR"  
    },  
    "diameter": {  
        "type": "Property",  
        "value": 203.00,  
        "unitCode": "MMT"  
    },  
    "roughness": {  
        "type": "Property",  
        "value": 72.4549,  
        "unitCode": "C62"  
    },  
    "minorLoss": {  
        "type": "Property",  
        "value": 72.4549,  
        "unitCode": "C62"  
    },  
    "tag": {  
        "type": "Property",  
        "value": "DMA1"  
    },  
     "description": {  
        "type": "Property",  
        "value": "Free Text"  
    },  
    "startsAt": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:Junction:63fe7d79-0d4c-4da9-b7d0-3340efa0656a"  
    },  
    "endsAt": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:Reservoir:1863179e-3768-4480-9167-ff21f870dd19"  
    },  
    "vertices": {  
        "type": "GeoProperty",  
        "value": {  
            "type": "MultiPoint",  
            "coordinates": [  
                [24.40623, 60.17966],  
                [24.50623, 60.27966]  
            ]  
        }  
    },  
    "bulkCoeff":{  
        "type": "Property",  
        "value": 72.4549,  
        "unitCode": "E91"  
    },  
    "wallCoeff":{  
        "type": "Property",  
        "value": 72.4549,  
        "unitCode": "RRC"  
    },  
    "@context": [  
        "https://schema.lab.fiware.org/ld/context"  
    ]  
}  
```  