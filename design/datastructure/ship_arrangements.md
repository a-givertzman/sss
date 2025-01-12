///
/// *Общее расположение*  
/// [ISO 10303-2015-2003](/reference/en/ISO/ISO%2010303-215-2004.pdf)  
**ship_arrangements**{  
    ///  
    /// *Идентификация грузов, перевозимых на судне*  
    /// [ISO 10303-2015-2003 p.4.1.2](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=21)  
    **cargoes**{  
        ///  
        //// *Груз - это любой предмет временного характера, загруженный на борт судна*  
        /// [ISO 10303-2015-2003 p.4.2.12](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=39)  
        /// [ISO 10303-2015-2003 p.5.1.3](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=230)  
        **cargo**[
            [cargo](temp/cargo.md)
        ]
        ///  
        /// *Расположение груза на судне*  
        /// [ISO 10303-2015-2003 p.4.2.13](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=41)  
        **Cargo_assignment**[
            [Cargo_assignment](Cargo_assignment.md)
        ]  
    }  
}  
