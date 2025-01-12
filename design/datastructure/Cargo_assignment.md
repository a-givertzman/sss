///  
/// *Расположение груза на судне*  
/// [ISO 10303-2015-2003 p.4.2.13](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=41)  
enum **Cargo_assignment**{
    ///
    /// *Груз распределен по отсеку или пространству внутри судна*  
    /// [ISO 10303-2015-2003 p.4.2.43](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=63)
    /// [ISO 10303-2015-2003 p.5.1.3.10](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=233)
    enum  **Compartment_cargo_assignment**{
        ///
        /// *Используется для bulk_cargo если перевозится насыпью*
        /// [ISO 10303-2015-2003 p.4.2.9](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=36)
        **Bulk_cargo_assignment**{
            ///
            /// *Высота груза*
            **cargo_height**
        }
        ///
        /// *Используется для или Gaseous_cargo если перевозится в газообразном состоянии*
        /// [ISO 10303-2015-2003 p.4.2.101](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=116)
        **Gaseous_cargo_assignment**{
        }
        ///
        /// *Используется для Liquid_cargo или Gaseous_cargo если перевозится в жидком состоянии*
        /// [ISO 10303-2015-2003 p.4.2.116](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=127)
        **Liquid_cargo_assignment**{
            ///
            /// *Высота груза*
            **cargo_height**
        }
    }
    **Compartment_cargo_assignment**{
        ///
        /// *Определяет тип груза, который был погружен*
        **cargo**{
            `id`
        }
        ///
        /// *Определяет отсек или пространство, в который был погружен груз*
        **compartment**{
            `id`
        }
    }
    ///
    /// *Груз Unit_cargo размещен на палубе(пока плохо понятна идеология зачем  надо Deck_cargo_assignment и Unit_cargo_assignment одновременно)*
    /// [ISO 10303-2015-2003 p.4.2.75](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=98)
    /// [ISO 10303-2015-2003 p.5.1.3.12](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=245)
    **Deck_cargo_assignment**{
        ///
        /// *Определяет груз Unit_cargo, который был погружен*
        **cargo**{
            `id`
        }
        ///
        /// *Определяет deck_zone, в который был погружен груз*
        **deck_zone**{
            `id`
        }
        /// *Определяет положение Unit_cargo на палубе, куда она была погружена*
        **position**{
            `X`,
            `Y`,
            `Z`
        }
    }
    ///
    /// *Размещение Unit_cargo с привязкой к отсеку или зоне на палубе (пока плохо понятна идеология зачем  надо Deck_cargo_assignment и Unit_cargo_assignment одновременно)*
    /// [ISO 10303-2015-2003 p.4.2.169](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=163)
    /// [ISO 10303-2015-2003 p.5.1.3.24](/reference/en/ISO/ISO%2010303-215-2004.pdf#page=272)
    **Unit_cargo_assignment**{
        ///
        /// *Определяет груз Unit_cargo, который был погружен*
        **cargo**{
            `id`
        }
        ///
        /// *Определяет тип позиции куда погружен Unit_cargo*
        **assigned_to**{
            `id`
        }
        /// *Позиция определяет положение Unit_cargo внутри отсека или на палубе, куда он был погружен*
        **position**{
            `X`,
            `Y`,
            `Z`
        }
    }
}  
**Cargo_assignment**{  
    ///  
    /// *Масса и центр тяжести груза*  
    **allocated_weight**{  
        `W,X,Y,Z`  
    }  
    ///  
    /// *Назначение груза*  
    enum **assignment_context**{  
        ///  
        /// *Полезный груз  для анализа проекта или для фактического рейса во время эксплуатации судна*  
        `cargo_load`,
        ///  
        /// *Груз является запасом для возможного использования пассажирами и экипажем в рейсе*  
        `stores`,  
        ///  
        /// *Назначение груза не определено*  
        `unspecified`  
    }  
    ///  
    /// *Уникальный номер груза*  
    **cargo_identifier**{  
        `id`  
    }  
}
