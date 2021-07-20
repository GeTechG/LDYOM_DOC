
View the fields of the [structures](https://github.com/GeTechG/LDYOM/blob/master/LDYOM_ASI/LDYOM_ASI/Init.h)

## lcapi_get_int_by_offset_address 0@ offset 1@ store_to 2@
``` c
1000: lcapi_get_int_by_offset_address 0@ offset 1@ store_to 2@
```
Get int at an offset address.

**0@** - structure address

**1@** - offset

**2@** - put where

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1000: lcapi_get_int_by_offset_address 1@ offset 88 store_to 2@
    ``` 




## lcapi_set_int_by_offset_address 0@ offset @1 value 2@
``` c
1001: lcapi_set_int_by_offset_address 0@ offset @1 value 2@
```
Set int at an offset address.

**0@** - structure address

**1@** - offset

**2@** - value

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1001: lcapi_set_int_by_offset_address 1@ offset 88 store_to 2@
    ``` 



## lcapi_get_float_by_offset_address 0@ offset 1@ store_to 2@
``` c
1002: lcapi_get_float_by_offset_address 0@ offset 1@ store_to 2@
```
Get float at an offset address.

**0@** - structure address

**1@** - offset

**2@** - put where

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1002: lcapi_get_float_by_offset_address 1@ offset 84 store_to 2@
    ``` 




## lcapi_set_float_by_offset_address 0@ offset @1 value 2@
``` c
1003: lcapi_set_float_by_offset_address 0@ offset @1 value 2@
```
Set float at an offset address.

**0@** - structure address

**1@** - offset

**2@** - value

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1003: lcapi_set_float_by_offset_address 1@ offset 84 store_to 2@
    ``` 



## lcapi_get_string_by_offset_address 0@ offset 1@ store_to 2@v
``` c
1004: lcapi_get_string_by_offset_address 0@ offset 1@ store_to 2@v
```
Get string at an offset address.

**0@** - structure address

**1@** - offset

**2@** - put where

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1004: lcapi_get_string_by_offset_address 1@ offset 88 store_to 2@vs
    ``` 




## lcapi_set_string_by_offset_address 0@ offset @1 value 2@v
``` c
1005: lcapi_set_string_by_offset_address 0@ offset @1 value 2@v
```
Set string at an offset address.

**0@** - structure address

**1@** - offset

**2@** - value

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1005: lcapi_set_string_by_offset_address 1@ offset 88 store_to 2@v
    ```


## lcapi_get_target 0@ store_to 1@
``` c
1006: lcapi_get_target 0@ store_to 1@
```
Tries to find a target with the given index and returns the address if found

**0@** - index target

**1@** - (address) put where

!!! example
    ``` c
    1006: lcapi_get_target 0@ store_to 1@
    1005: lcapi_set_string_by_offset_address 1@ offset 88 store_to 2@v
    ``` 

## lcapi_get_actor 0@ store_to 1@
``` c
1006: lcapi_get_actor 0@ store_to 1@
```
Tries to find a actor with the given index and returns the address if found.

**0@** - index target

**1@** - (address) put where

!!! example
    ``` c
    1006: lcapi_get_actor 0@ store_to 1@
    1005: lcapi_set_string_by_offset_address 1@ offset 0 store_to 2@v
    ``` 

## lcapi_get_address_element_vector type 0@ address 1@ index 2@ store_to 3@
``` c
1007: lcapi_get_address_element_vector type 0@ address 1@ index 2@ store_to 3@
```
Searches for an element in a vector and returns it.

**0@** - type

    0 - int
    1 - float
    2 - string (char*)
    3 - string (std::string)
    4 - Dialog

**1@** - address

**2@** - element index

**3@** - (value/address) put where

!!! example
    ``` c
    1006: lcapi_get_actor 0@ store_to 1@
    1007: lcapi_get_address_element_vector type 0 address 1@ index 2@ store_to 3@
    ``` 

## lcapi_set_address_element_vector type 0@ address 1@ index 2@ value 3@
``` c
1007: lcapi_set_address_element_vector type 0@ address 1@ index 2@ value 3@
```
Searches for an element in a vector and assigns a value to it.

**0@** - type

    0 - int
    1 - float
    2 - string (char*)
    3 - string (std::string)
    4 - Dialog

**1@** - address

**2@** - element index

**3@** - value/address

!!! example
    ``` c
    1006: lcapi_set_actor 0@ store_to 1@
    1007: lcapi_set_address_element_vector type 0 address 1@ index 2@ value 3@
    ``` 