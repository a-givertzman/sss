Ship{
    // [ISO 10303-2016-2003, 4.2.22]()
    description{
        /// Описание 
    }
    name{
        /// Наименование
    }
    ship to external_reference (as documentation){
        /// документация
    }
    ship to global_id (as id){
        /// Номер идентификационный
    }
    ship to item (as ship_items){
        /// Или Ship_moulded_form или Moulded_form
    }
    single_hull_or_class{
        /// один корпус или несколько
    }
    ship to derived_unit (as units)
    ship to named_unit (as units)
}