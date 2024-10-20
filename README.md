import random

plan_tranquilo = ["Paseo por la costa", "Sesión de pelis/series",  "Paseo por Las Palmas GC", "Jugar bolos/billar", "Tomar algo en un bar", "Visitar algún museo"]

plan_movido = ["Senderismo por el campo", "Senderismo playero", "Senderismo por barrancos", "Paseo por la cumbre/Tejeda", "Ruta miradores"]

plan_mixto = ["Playa del sur", "Playa del norte", "Playa del sureste", "Playa del este", "Ruta en coche", "Vuelta a la isla", "Visitar un pueblo random en el norte", "Visitar un pueblo random en el sur/sureste", "Visitar un pueblo random en el este/centro"]

election = ""
while election not in ["tranquilo", "movido", "mixto"]:
    election = input("Elige un plan (tranquilo, movido o mixto): ").strip().lower()

    if election == "tranquilo":
        user_plan = random.choice(plan_tranquilo)
        
    elif election == "movido":
        user_plan = random.choice(plan_movido)
        
    elif election == "mixto":
        user_plan = random.choice(plan_mixto)
        
    else:
        print("Pon una opción válida")
        user_plan = None
        
if user_plan:
    print((f"Mi propuesta es: {user_plan}"))
