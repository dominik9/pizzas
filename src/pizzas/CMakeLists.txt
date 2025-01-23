add_library(pizzas 
    Funghi.cpp
    Margherita.cpp
    Pizza.cpp
    Pizzeria.cpp
)

target_include_directories(pizzas PUBLIC include)