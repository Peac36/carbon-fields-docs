# Network

Network container is similar to the Theme Options. However, the container's fields are visible only in the Network Dashboard.

```php
use Carbon_Fields\Container;
use Carbon_Fields\Field;

Container::make( 'network', 'Network Options' )
    ->add_fields( array(
        Field::make( 'text', 'crb_network_title') ,
        Field::make( 'textarea', 'crb_network_description' )
    ) );
```

By default, the container stores the values in the site specified by `SITE_ID_CURRENT_SITE` constant.(see [Create a network](https://codex.wordpress.org/Create_A_Network))

### Site ID

Specify in which site to store all container's fields values.

`->set_site_id( $site_id )`

### Accessing field values

Retrieving the container's fields values go through `carbon_get_the_network_option( $name )` and  `carbon_get_network_option( $id, $name )`.

| Parameter            | Description                                                                         |
| -------------------- | ----------------------------------------------------------------------------------- |
| `$id`                | The ID on site where meta is stored.                                               |
| `$name`              | The field name pattern of the field to be retrieved.                                              |
