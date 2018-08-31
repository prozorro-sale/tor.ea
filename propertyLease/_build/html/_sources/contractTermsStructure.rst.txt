.. _contractTermsStructure:

Структура даних: contractTerms
==============================

.. literalinclude:: js/Contractterms.http
   :language: javascript

.. _contractTerms:

contractTerms
-------------

:type:
  обов’язково. Єдине можливе значення:lease 

  Тип умов контракту.

:leaseTerms:
  масив :ref:`leaseTerms`

  Блок, що містить інформацію про термінита особливі умови оренди.

.. _leaseTerms:

leaseTerms
----------

:leaseDuration:
  :ref:`Durations`, обов’язково

  Тривалість оренди .

:taxHolidays:
  масив :ref:`taxHolidays`, не обов’язково

  Орендні канікули.

:escalationClauses:
  :ref:`escalationClauses`, не обов’язково

  Індексація ціни.

.. _taxHolidays:

taxHolidays
-----------

:id:
  унікальний ідентифікатор, автогенерований, тільки для читання

  Ідентифікатор об’єкту.

:taxHolidaysDuration:
  :ref:`Durations`, обов’язково

  Тривалість орендних канікул.

:conditions:
  рядок, обов’язково для української мови, багатомовний

    Умови на час орендних канікул. Вказується українською.

    * conditions_en - Вказується англійською.

    * conditions_ru - Вказується російською.

:value:
  :ref:`value`, обов'язково

  Загальна вартість оренди

.. _value:

Value
-----

:amount:
  десяткове число, обов’язково

  Вартість оренди на час орендних канікул.

:currency:
  рядок, обов’язково

  Валюта вартості оренди на час орендних канікул. Єдине доступне значення UAH.

:valueAddedTaxIncluded:
  булеве значення, обов’язково

  Факт урахування ПДВ. Допустимі значення: ``true`` або ``false``.

.. _escalationClauses:

escalationClauses
-----------------

:id:
  унікальний ідентифікатор, автогенерований, тільки для читання

  Ідентифікатор об’єкту

:escalationPeriodicity:
  :ref:`Durations`, обов’язково

  Періодичність, з якою здійснюватиметься індексування вартості.

:escalationStepPercentageRange:
  десяткове число, обов’язково

  Відсоток, в межах якого здійснюватиметься індексування вартості

:conditions:
  рядок, обов’язково для української мови, багатомовний

  Умови проведення індексування. Вказується українською.

    * conditions_en - Вказується англійською.

    * conditions_ru - Вказується російською.

.. _Durations:

Тривалість
----------

Тривалість у форматі `ISO 8601 <https://en.wikipedia.org/wiki/ISO_8601#Durations>`_.

