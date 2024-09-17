# Ac.MyID.Proxy.V1
1. [Данные авторизации](#Данные-авторизации)
	1. [Результат обработки персональных данных по job_id](#Результат-обработки-персональных-данных-по-job_id)
	2. [Запрос на обработку персональных данных](#Запрос-на-обработку-персональных-данных)
## <a name="Данные-авторизации">Данные авторизации</a>
### <a name="Результат-обработки-персональных-данных-по-job_id">Результат обработки персональных данных по job_id</a>
Endpoint ESB: **POST** **/api/v1/authentication/simple-inplace-authentication-request-status** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(Query-params)***|||
|job_id|Идентификатор обработки запроса|string|
#### Параметры ответа
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|comparison_value|Результат сравнения (0.5-1.0 успешно)|number|
|**profile**|Профиль|object|
|**profile.address**|Адрес|object|
|**profile.address.temporary_registration**|Прописка|object|
|profile.address.temporary_registration.date_from|Дата начала регистрации|string|
|profile.address.temporary_registration.district_id|Идентификационный номер района/города (По справочнику МВД)|string|
|profile.address.temporary_registration.region_id|Идентификационной номер региона (по справочнику МВД)|string|
|profile.address.temporary_registration.region_id_cbu|Идентификационной номер региона (по справочнику ЦБ)|string|
|profile.address.temporary_registration.cadastre|Кадастровый номер|string|
|profile.address.temporary_registration.country_id|Идентификационный номер страны (По справочнику МВД)|string|
|profile.address.temporary_registration.country_id_cbu|Идентификационный номер страны (По справочнику ЦБ)|string|
|profile.address.temporary_registration.district|Значение района (города)|string|
|profile.address.temporary_registration.district_id_cbu|Идентификационный номер района/города (По справочнику ЦБ)|string|
|profile.address.temporary_registration.region|Значение региона|string|
|profile.address.temporary_registration.address|Адрес|string|
|profile.address.temporary_registration.country|Значение страны|string|
|profile.address.temporary_registration.date_till|Дата окончания регистрации|string|
|profile.address.permanent_address|Адрес постоянной регистрации|string|
|**profile.address.permanent_registration**|Прописка|object|
|profile.address.permanent_registration.registration_date|Дата регистрации|string|
|profile.address.permanent_registration.address|Адрес|string|
|profile.address.permanent_registration.cadastre|Кадастровый номер|string|
|profile.address.permanent_registration.country|Значение страны|string|
|profile.address.permanent_registration.country_id|Идентификационный номер страны (По справочнику МВД)|string|
|profile.address.permanent_registration.country_id_cbu|Идентификационный номер страны (По справочнику ЦБ)|string|
|profile.address.permanent_registration.region_id|Идентификационной номер региона (по справочнику МВД)|string|
|profile.address.permanent_registration.region_id_cbu|Идентификационной номер региона (по справочнику ЦБ)|string|
|profile.address.permanent_registration.district|Значение района (города)|string|
|profile.address.permanent_registration.district_id|Идентификационный номер района/города (По справочнику МВД)|string|
|profile.address.permanent_registration.district_id_cbu|Идентификационный номер района/города (По справочнику ЦБ)|string|
|profile.address.permanent_registration.region|Значение региона|string|
|profile.address.temporary_address|Адрес временной регистрации|string|
|profile.authentication_method|Метод аутентификации (simple, strong)|string|
|**profile.common_data**|Общие данные|object|
|profile.common_data.gender|Пол (1- Мужчина, 2- Женщина)|string|
|profile.common_data.inn|Идентификационной номер налогоплательщика|string|
|profile.common_data.last_name|Фамилия|string|
|profile.common_data.last_update_inn|Дата и время последнего обновления в системе идентификационного номера налогоплательщика|string|
|profile.common_data.birth_country_id|Идентификатор страны рождения (по справочнику ГЦП)|string|
|profile.common_data.birth_country_id_cbu|Идентификатор страны рождения (по справочнику ЦБ)|string|
|profile.common_data.birth_place|Место рождения|string|
|profile.common_data.citizenship_id|Идентификатор гражданства (по справочнику ГЦП)|string|
|profile.common_data.sdk_hash|Хэш код, который можно направить в последующих запросах в SDK (вместо реквизитов документа, удостоверяющего личность и даты рождения) в целях получения данных пользователя|string|
|profile.common_data.last_update_address|Дата и время последнего обновления в системе адреса регистрации|string|
|profile.common_data.last_update_pass_data|Дата и время последнего обновления в системе документа, удостоверяющего личность|string|
|profile.common_data.nationality|Национальность|string|
|profile.common_data.birth_country|Страна рождения|string|
|profile.common_data.citizenship|Гражданство|string|
|profile.common_data.citizenship_id_cbu|Идентификатор гражданства (по справочнику ЦБ)|string|
|profile.common_data.last_name_en|Фамилия на английском языке|string|
|profile.common_data.birth_date|Дата рождения|string|
|profile.common_data.middle_name|Отчество|string|
|profile.common_data.pinfl|Персональный идентификационной номер физического лица|string|
|profile.common_data.first_name|Имя|string|
|profile.common_data.first_name_en|Имя на английском языке|string|
|profile.common_data.nationality_id|Идентификатор национальности (по справочнику ГЦП)|string|
|profile.common_data.nationality_id_cbu|Идентификатор национальности (по справочнику ЦБ)|string|
|**profile.contacts**|Контакты|object|
|profile.contacts.email|Адрес электронной почты|string|
|profile.contacts.phone|Номер телефона|string|
|**profile.doc_data**|Документ, удостоверяющий личность|object|
|profile.doc_data.doc_type_id|Идентификатор типа документа|string|
|profile.doc_data.doc_type_id_cbu|Идентификатор типа документа (по справочник ЦБ)|string|
|profile.doc_data.expiry_date|Срок действия|string|
|profile.doc_data.issued_by|Место выдачи|string|
|profile.doc_data.issued_by_id|Идентификатор места выдачи|string|
|profile.doc_data.issued_date|Дата выдачи|string|
|profile.doc_data.pass_data|Серия и номер|string|
|profile.doc_data.doc_type|Тип документа|string|
|response_id|Идентификатор ответа|string|
|result_code|Код результата ответа (0 – успешно)|number|
|result_note|Описание результата ответа|string|
##### HTTP-Code 202 ACCEPTED
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 400 BAD_REQUEST
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 403 FORBIDDEN
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 422 UNPROCESSABLE_ENTITY
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|**body**|Тело запроса с ошибкой|object|
|**detail**|Сведения об ошибке|array|
|**detail[i].loc**|Локация отсутствующих полей|array|
|detail[i].msg|Сообщение|string|
|detail[i].type|Тип ошибки|string|
##### HTTP-Code 500 INTERNAL_SERVER_ERROR
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
### <a name="Запрос-на-обработку-персональных-данных">Запрос на обработку персональных данных</a>
Endpoint ESB: **POST** **/api/v1/authentication/simple-inplace-authentication-request-task** Формат **json**
#### Параметры запроса
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|threshold|Значение сравнения фотографий от 0.5 до 1.0|number|
|birth_date|Дата рождения|string|
|device|Данные об устройстве пользователя|string|
|external_id|Идентификатор запроса клиента|string|
|pass_data|Серия и номер паспорта|string|
|**photo_from_camera**|Фотографии лица|object|
|photo_from_camera.front|Фото – лицо смотрит прямо (в формате Data URI)|string|
|pinfl|ПИНФЛ пользователя|string|
|agreed_on_terms|Согласие физического лица на обработку его персональных данных|boolean|
|client_id|Идентификатор клиента|string|
#### Параметры ответа
##### HTTP-Code 500 INTERNAL_SERVER_ERROR
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 200 OK
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|job_id|Идентификатор обработки запроса|string|
##### HTTP-Code 202 ACCEPTED
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 400 BAD_REQUEST
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 403 FORBIDDEN
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
##### HTTP-Code 422 UNPROCESSABLE_ENTITY
|**Наименование параметра**|**Описание**|**Тип**|
|-|-|-|
|***(HTTP-Body)***|||
|**body**|Тело запроса с ошибкой|object|
|**detail**|Сведения об ошибке|array|
|detail[i].type|Тип ошибки|string|
|**detail[i].loc**|Локация отсутствующих полей|array|
|detail[i].msg|Сообщение|string|
