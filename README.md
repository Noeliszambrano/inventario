# inventario
inventory = {
   "1" : {"name": "arroz", "price": "2800", "available_quantity": "15"},
    "2" : {"name": "sal", "price": "1800", "available_quantity": "6"},
    "3" : {"name": "aceite", "price": "5700", "available_quantity": "4"},
    "4" : {"name": "pasta", "price": "4600", "available_quantity": "8"},
    "5" : {"name": "chocolate", "price": "7500", "available_quantity": "3"},
    "6" : {"name": "papa", "price": "2200", "available_quantity": "5"},
    "7" : {"name": "pollo", "price": "16000", "available_quantity": "7"},
    "8" : {"name": "fideos", "price": "2400", "available_quantity": "12"},
    "9" : {"name": "leche", "price": "3400", "available_quantity": "9"},
    "10" : {"name": "azucar", "price": "4600", "available_quantity": "7"},
}
print(inventory)
DANGER = "\033[91m"
WARNING = "\033[93m"
SUCCESS = "\033[92m"
RESET = "\033[0m"

def add_products():
    name = input("ingrese el nombre del nuevo producto: ")
    price = input("ingrese el precio del nuevo producto: ")
    available_quantity = input("ingrese la cantidad disponible del nuevo producto: ")
    if name:
     print(DANGER + "Producto existente. " + RESET)
    else:
     print(SUCCESS + "Nuevo producto agregado de manera exitosa." + RESET)  
add_products()

def search():
    name = input("ingrese el nombre del producto a buscar: ")
    if name in {}:
        print(SUCCESS + "producto encontrado" + RESET)
    else:
        print(WARNING + "Este producto no existe" + RESET)
search()

def update():
    name = input("ingrese el nombre del producto que desea actualizar: ")
    if name:
       name = input("ingrese el nombre: ")
       price = input("ingrese el precio: ")
       available_quantity = input("ingrese la cantidad de productos: ")
       print(SUCCESS + "actualizacion exitosa. " + RESET)
    else:
     print(DANGER + "no se puso actualizar. " + RESET)
update()

def delete():
    name = input("ingrese el nombre del producto que desea eliminar: ")
    if name:
        inventory.pop (name,[name])
        print(SUCCESS + "Producto eliminado. " + RESET)
    else:
        print(WARNING + "No se pudo eliminar." + RESET)
delete()
