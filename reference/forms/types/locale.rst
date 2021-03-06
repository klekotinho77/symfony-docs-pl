.. index::
   single: Forms; Fields; locale

locale Typ Pola
===============

Typ ``locale`` jest podzbiorem ``ChoiceType`` który umożliwia użytkownikowi
wybranie spośród dużej listy, lokalizację (język+kraj). Dodatkowym bonusem, jest
to że nazwy lokalizacji są wyświetlone w języku użytkownika.

"Wartością" dla każdej lokalizacji jest dwuliterowy kod *języka* zgodny z ISO639-1
(np. ``pl``), lub kod języka z znakiem podkreślenia (``_``), oraz kod *kraju* zgodny
z ISO3166 (np. ``pl_PL`` dla Polskiego/Polski).

.. note::

    Lokalizacja Twojego użytkownika jest pobierana poprzez `Locale::getDefault()`_

W przeciwieństwie do typu ``choice``, nie musisz definiować opcji ``choices`` lub ``choice_list``, 
ponieważ pole automatycznie wypełni je dużą listą lokalizacji. *Możesz* zdefiniować 
te opcje ręcznie, w takim przypadku musisz użyć bezpośrednio opcji ``choice``.

+------------------+---------------------------------------------------------------------------------------------+
| Renderowane jako | może być generowane na kilka sposobów (zobacz :ref:`forms-reference-choice-tags`)           |
+------------------+---------------------------------------------------------------------------------------------+
| Odziedziczone    | - `multiple`_                                                                               |
| opcje            | - `expanded`_                                                                               |
|                  | - `preferred_choices`_                                                                      |
|                  | - `empty_value`_                                                                            |
|                  | - `error_bubbling`_                                                                         |
|                  | - `required`_                                                                               |
|                  | - `label`_                                                                                  |
|                  | - `read_only`_                                                                              |
+------------------+---------------------------------------------------------------------------------------------+
| Rodzic           | :doc:`choice</reference/forms/types/choice>`                                                |
+------------------+---------------------------------------------------------------------------------------------+
| Klasa            | :class:`Symfony\\Component\\Form\\Extension\\Core\\Type\\LanguageType`                      |
+------------------+---------------------------------------------------------------------------------------------+

Odziedziczone opcje
-------------------

Opcje te są odziedziczone z typu :doc:`choice</reference/forms/types/choice>`:

.. include:: /reference/forms/types/options/multiple.rst.inc

.. include:: /reference/forms/types/options/expanded.rst.inc

.. include:: /reference/forms/types/options/preferred_choices.rst.inc

.. include:: /reference/forms/types/options/empty_value.rst.inc

.. include:: /reference/forms/types/options/error_bubbling.rst.inc

Opcje te są odziedziczone z typu :doc:`field</reference/forms/types/field>`:

.. include:: /reference/forms/types/options/required.rst.inc

.. include:: /reference/forms/types/options/label.rst.inc

.. include:: /reference/forms/types/options/read_only.rst.inc

.. _`Locale::getDefault()`: http://php.net/manual/en/locale.getdefault.php
