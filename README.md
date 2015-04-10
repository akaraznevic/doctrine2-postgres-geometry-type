Provides Postgres Geometry Type for Doctrine2
-------------------------------------------
Provides Doctrine Type class for postgres geometry type

#### Using with Zend Framework 2

Add this to `config\autoload\global.php`

    <?php

    return array(
        'doctrine' => array(
            'connection' => array(
                'orm_default' => array(
                 ...
                )
            ),
            'configuration' => array(
                'orm_default' => array(
                    'types' => array(
                        'geometry' => 'YouProjectNamespace\Doctrine\Types\GeometryType'
                    )
                )
            )
        )
     );

Usage in Entity class

     <?php

     /**
      * Class SuperEntity
      * @Entity
      * @Table(name="super-table")
      */
     class SuperEntity
     {
         /**
          * @var int
          *
          * @Id @Column(type="integer")
          * @GeneratedValue
          */
         private $id;

         /**
          * @var string
          *
          * @Column(type="geometry", name="geometry")
          */
         private $geometry;

#### License

Licensed under the MIT License