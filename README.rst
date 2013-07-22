=====================
django_localflavor_mx
=====================

Country-specific Django helpers for Mexico.

=======
WARNING
=======

This app has been superseded by the newly created django-localflavor_ app
which recombines all the different country locaflavors again (after having
been removed from Django). Development and maintenance of this app has
stopped and is only left online as a reminder for the users of those apps.
It will be removed after grace period of 1 Django release (~spring 2014).

.. _django-localflavor: https://github.com/django/django-localflavor/

What's in the Mexico localflavor?
=================================

* forms.MXZipCodeField: A form field that accepts a Mexican Zip Code. More info
  about this: List of postal codes in Mexico (zipcodes_)

* forms.MXRFCField: A form field that validates a Mexican *Registro Federal de
  Contribuyentes* for either **Persona física** or **Persona moral**. This
  field accepts RFC strings whether or not it contains a *homoclave*. More info
  about this: Registro Federal de Contribuyentes (rfc_)

* forms.MXCURPField: A field that validates a Mexican *Clave Única de Registro
  de Población*. More info about this: Clave Unica de Registro de Poblacion
  (curp_)

* forms.MXStateSelect: A ``Select`` widget that uses a list of Mexican states
  as its choices.

* forms.MXSocialSecurityNumberField: A field that validates a Mexican Social
  Security Number(NSS) for *Instituto Mexicano del Seguro Social*.

* models.MXStateField: A model field that stores the three-letter Mexican state
  abbreviation in the database.

* models.MXZipCodeField: A model field that forms represent as a
  ``forms.MXZipCodeField`` field and stores the five-digit Mexican zip code.

* models.MXRFCField: A model field that forms represent as a
  ``forms.MXRFCField`` field and stores the value of a valid Mexican RFC.

* models.MXCURPField: A model field that forms represent as a
  ``forms.MXCURPField`` field and stores the value of a valid Mexican CURP.

* models.MXSocialSecurityNumberField: A model field that forms represent as a
  ``forms.MXSocialSecurityNumberField`` field and stores the eleven-digit
  Mexican Social Security Number for *Instituto Mexicano del Seguro Social*.

Additionally, a choice tuple is provided in ``django_localflavor_mx.mx_states``,
allowing customized model and form fields, and form presentations, for subsets of
Mexican states abbreviations:

* mx_states.STATE_CHOICES: A tuple of choices of the states abbreviations for
  all 31 Mexican states, plus the `Distrito Federal`.

.. _zipcodes: http://en.wikipedia.org/wiki/List_of_postal_codes_in_Mexico
.. _rfc: http://es.wikipedia.org/wiki/Registro_Federal_de_Contribuyentes_(M%C3%A9xico)
.. _curp: http://www.condusef.gob.mx/index.php/clave-unica-de-registro-de-poblacion-curp

See the source code for full details.

About localflavors
==================

Django's "localflavor" packages offer additional functionality for particular
countries or cultures.

For example, these might include form fields for your country's postal codes,
phone number formats or government ID numbers.

This code used to live in Django proper -- in django.contrib.localflavor -- but
was separated into standalone packages in Django 1.5 to keep the framework's
core clean.

For a full list of available localflavors, see https://github.com/django/
