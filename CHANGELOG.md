### 2.9.0
* enhancements
    * removed the ```http://www.w3.org/2001/XMLSchema``` and ```http://www.w3.org/2001/XMLSchema-instance``` namespaces from the ```to_soap``` method.

### 2.8.1
* enhancements
    * changed the ```#attribute_value=``` method on ```ComplexTypes::AttributeValue``` so it will replace the existing attribute values, instead of appending to it

### 2.8.0
* enhancements
    * added ```AttributeValue``` element
    * added the possibility to have many ```AttributeValue``` elements on elements which include the ```ComplexTypes::AttributeType```
    * the ```#attribute_value``` method on ```ComplexTypes::AttributeType``` is now deprecated

### 2.7.0
* updated xmlenc dependency
* enhancements
    * added the possibility to use a ```KeyDescriptor``` in the ```Util::EncryptAssertion``` method, so we can set the ```key_name``` in the encrypted assertion.

### 2.6.9
* enhancements
    * added ```name_id_formats``` to the ```SSODescriptorType``` complex type.

### 2.6.8
* enhancements
    * added the option to set a custom endpoint index for an ```Artifact```.

### 2.6.7
* enhancements
    * fixed a parsing bug where an unsigned ```ArtifactResponse``` received the signature of its inner signed message.

### 2.6.5
* enhancements
    * added ```authn_request``` element on an ```ArtifactResponse``` so that both a ```Response``` as well as an ```AuthnRequest``` can be transferred.

### 2.6.4
* enhancements
    * added ```attribute_authority_descriptor``` element, which extends the ```RoleDescriptorType``` complex type, to an ```entity_descriptor``` element
    * added ```role_descriptor_type``` complex type

### 2.6.3
* enhancements
    * added ```status_detail``` element

### 2.6.2
* enhancements
    * added metadata publication info element

### 2.6.1
* enhancements
    * added ```fetch_attributes``` method to fetch multiple attributes with the same name from an assertion

### 2.6.0
* updated xmlenc dependency

### 2.5.1
* enhancements
    * allow metadata ```key_descriptor``` use to be omitted and be used as default

### 2.5.0
* enhancements
    * added backwards compatible ```has_many``` for ```authn_context_class_refs``` so the SP can request more than one context

### 2.4.1
* enhancements
    * use a hash for the file store
    * allow metadata to be added to the file store on the fly

### 2.3.2
* bug fix
    * fixed alias method error

### 2.3.1
* enhancements
    * started this changelog
    * Added a new url provider store use:
    ```Saml::ProviderStores::Url.find_by_metadata_location(metadata_location)``` or
    ```Saml::ProviderStores::Url.find_by_entity_id(metadata_location)``` # allow use through ```Saml.provider(entity_id)```
    * Added the entity id to the error message when ```Saml.provider``` cannot find ```entity id```
