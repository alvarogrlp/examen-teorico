# examen-teorico

## Actores

### Actor: Cliente
| Actor | Cliente |
|---|---|
| **Descripción**  | Representa a los usuarios que interactúan con el sistema VIDEOMAX para alquilar, devolver o reservar películas. |
| **Características**  | Usuario externo que proporciona datos personales, alquila películas, devuelve películas y realiza reservas. |
| **Relaciones** | Comparte acciones con el administrador, como la selección de películas y la interacción con el registro de alquileres o reservas. |
| **Referencias** | Casos de uso relacionados: "Proporciona Datos Personales", "Alquila Película", "Devuelve Película", "Reserva Película". |   
| **Notas** | Debe estar registrado en el sistema para acceder a los servicios. |
| **Autor**  | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Actor: Administrador VIDEOMAX
| Actor | Administrador VIDEOMAX |
|---|---|
| **Descripción**  | Representa al encargado de gestionar las películas, reservas, alquileres y clientes en el sistema VIDEOMAX. |
| **Características**  | Usuario interno que registra clientes, actualiza proveedores y administra las películas. |
| **Relaciones** | Interactúa directamente con los clientes y el proveedor para garantizar el funcionamiento del sistema. |
| **Referencias** | Casos de uso relacionados: "Registra a los Clientes", "Registra Película", "Registra Alquiler", "Registra Reserva". |   
| **Notas** | Tiene acceso a las funcionalidades administrativas del sistema. |
| **Autor**  | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Actor: Proveedor
| Actor | Proveedor |
|---|---|
| **Descripción**  | Representa a la entidad que abastece películas al sistema según la disponibilidad. |
| **Características**  | Usuario externo que suministra películas al sistema VIDEOMAX. |
| **Relaciones** | Colabora con el administrador para asegurar la existencia de películas en el catálogo. |
| **Referencias** | Casos de uso relacionados: "Abastece Película Según Existencia", "Abastece Película", "Actualiza Proveedor". |   
| **Notas** | Su rol es clave para mantener el inventario actualizado. |
| **Autor**  | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

## Casos de Uso

### Caso de Uso: Proporciona Datos Personales
| Caso de Uso CU | Proporciona Datos Personales |
|---|---|
| **Fuentes** | Especificación del sistema VIDEOMAX. |
| **Actor** | Cliente |
| **Descripción** | El cliente proporciona sus datos personales para ser registrado en el sistema. |
| **Flujo básico** | 1. El cliente ingresa sus datos personales.<br>2. El sistema valida la información.<br>3. El sistema registra al cliente. |
| **Pre-condiciones** | El cliente no debe estar registrado previamente. |
| **Post-condiciones** | Los datos del cliente se guardan en la base de datos. |
| **Requerimientos** | El cliente debe proporcionar información válida (nombre, dirección, etc.). |
| **Notas** | Este paso es necesario para que el cliente pueda realizar otras operaciones en el sistema. |
| **Autor** | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Caso de Uso: Alquila Película
| Caso de Uso CU | Alquila Película |
|---|---|
| **Fuentes** | Especificación del sistema VIDEOMAX. |
| **Actor** | Cliente |
| **Descripción** | El cliente selecciona una película y completa el proceso de alquiler. |
| **Flujo básico** | 1. El cliente selecciona la película.<br>2. El cliente proporciona los datos necesarios.<br>3. El sistema registra el alquiler. |
| **Pre-condiciones** | El cliente debe estar registrado y la película debe estar disponible. |
| **Post-condiciones** | La película queda marcada como alquilada en el sistema. |
| **Requerimientos** | La película debe estar disponible en el catálogo. |
| **Notas** | El sistema envía un comprobante al cliente tras completar el alquiler. |
| **Autor** | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Caso de Uso: Devuelve Película
| Caso de Uso CU | Devuelve Película |
|---|---|
| **Fuentes** | Especificación del sistema VIDEOMAX. |
| **Actor** | Cliente |
| **Descripción** | El cliente devuelve una película previamente alquilada. |
| **Flujo básico** | 1. El cliente entrega la película.<br>2. El sistema actualiza el estado de la película como disponible.<br>3. Se registra la devolución en el sistema. |
| **Pre-condiciones** | La película debe haber sido previamente alquilada por el cliente. |
| **Post-condiciones** | La película queda disponible para nuevos alquileres. |
| **Requerimientos** | La película debe estar físicamente devuelta. |
| **Notas** | Si hay retrasos, el sistema puede registrar una multa. |
| **Autor** | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Caso de Uso: Reserva Película
| Caso de Uso CU | Reserva Película |
|---|---|
| **Fuentes** | Especificación del sistema VIDEOMAX. |
| **Actor** | Cliente |
| **Descripción** | El cliente reserva una película para garantizar su disponibilidad. |
| **Flujo básico** | 1. El cliente selecciona la película.<br>2. El sistema verifica la disponibilidad.<br>3. Se registra la reserva en el sistema. |
| **Pre-condiciones** | La película debe estar disponible para reserva. |
| **Post-condiciones** | La película queda marcada como reservada en el sistema. |
| **Requerimientos** | El cliente debe estar registrado y la película no debe estar alquilada. |
| **Notas** | La reserva tiene una duración limitada antes de expirar. |
| **Autor** | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Caso de Uso: Registra Película
| Caso de Uso CU | Registra Película |
|---|---|
| **Fuentes** | Especificación del sistema VIDEOMAX. |
| **Actor** | Administrador VIDEOMAX |
| **Descripción** | El administrador agrega una nueva película al catálogo del sistema. |
| **Flujo básico** | 1. El administrador ingresa los datos de la película.<br>2. El sistema valida la información.<br>3. Se registra la película en el catálogo. |
| **Pre-condiciones** | El administrador debe tener acceso al sistema. |
| **Post-condiciones** | La película queda disponible para alquiler o reserva. |
| **Requerimientos** | El sistema debe permitir el ingreso de datos de películas. |
| **Notas** | La información de la película debe ser precisa para evitar errores en el catálogo. |
| **Autor** | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |

---

### Caso de Uso: Abastece Película
| Caso de Uso CU | Abastece Película |
|---|---|
| **Fuentes** | Especificación del sistema VIDEOMAX. |
| **Actor** | Proveedor |
| **Descripción** | El proveedor suministra películas al sistema según la existencia y necesidad del catálogo. |
| **Flujo básico** | 1. El proveedor revisa el inventario.<br>2. Abastece películas según disponibilidad.<br>3. El sistema actualiza el inventario. |
| **Pre-condiciones** | El proveedor debe estar registrado en el sistema. |
| **Post-condiciones** | El catálogo se actualiza con las películas abastecidas. |
| **Requerimientos** | Las películas deben ser entregadas físicamente. |
| **Notas** | Este caso de uso garantiza que el sistema tenga suficiente inventario para atender a los clientes. |
| **Autor** | alvarogrlp |
| **Fecha** | 20 de noviembre de 2024 |


