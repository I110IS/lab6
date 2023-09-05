# LAB6

## Objetivos

Cómo generar PDFs, cargar archivos y manejar puntos geográficos.

## Pasos previos

Ver la sección [preparar repositorio](https://github.com/I110IS/lab1/blob/master/README.md#preparar-repositorio)

## Parte 1 - APIs

Vamos a validar que los teléfonos de los monstruos sean válidos usando https://www.abstractapi.com/api/phone-validation-api#docs

1. Crear una cuenta en https://app.abstractapi.com/users/signup?target=/api/phone-validation/pricing/select (elegir el plan gratuito)
1. Guardar la API key en las credenciales de rails
1. Actualizar la acción de crear y actualizar monstruos para que se valide que el teléfono sea válido y de Argentina. Si el teléfono no cumple con alguna de esas condiciones se deberá indicar al usuario con un mensaje de error que explique el motivo.

## Parte 2 - Puntos geográficos

1. Agregar una columna de tipo `point` para guardar la latitud y longitud de dónde se creó un tweet.
1. Actualizar el formulario de tweets para enviar la latitud y longitud del monstruo al crear el tweet.
1. Actualizar el controlador para recibir la latitud y longitud y guardarlo en el tweet.
1. Actualizar `tweets#show` para mostrar en un mapa la ubicación desde donde fue enviado el tweet.
    1. No mostrar mapa si el tweet no tiene información geográfica.
1. Guardar la ubicación actual del usuario en la sesión.
1. Actualizar el `tweets#index` para que en el listado de tweets se muestren primero los tweets más cercanos al usuario.
1. Actualizar el `tweets#index` para mostrar únicamente los tweets dentro del casco urbano platense cuando se reciba el parametro `lp=true`.
1. Actualizar el `tweets#show` para mostrar la dirección desde donde fue creado el tweet.
    1. Se puede usar https://www.geoapify.com/reverse-geocoding-api (Ver laboratorio sobre APIs externas)
