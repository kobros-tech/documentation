============
New vehicles
============

Odoo's *Fleet* app manages all vehicles and the accompanying documentation that comes with vehicle
maintenance and driver's records.

All vehicles are organized on the main :guilabel:`Fleet` dashboard. Each vehicle has its own
*vehicle form*, which is displayed as a card in the kanban view, according to it's status. Every
vehicle form is displayed in its current corresponding kanban stage. The default stages are
:guilabel:`New Request`, :guilabel:`To Order`, :guilabel:`Registered`, and :guilabel:`Downgraded`.

To add a new vehicle to the fleet, click the :guilabel:`New` button in the top-left corner, and a
blank vehicle form loads. Enter the vehicle information in the vehicle form. The form auto-saves as
data is entered.

.. _fleet/new_vehicle/vehicle-form:

Vehicle form fields
===================

- :guilabel:`Model`: select the vehicle's model from the drop-down menu. If the model is not listed,
  type in the model name and click either :guilabel:`Create "model"` or :guilabel:`Create and
  edit...` to :ref:`create a new model and edit the model details <fleet/configuration/add-model>`.
- :guilabel:`License Plate`: enter the vehicle's license plate number in this field.
- :guilabel:`Tags`: select any tags from the drop-down menu, or type in a new tag. There is no limit
  on the amount of tags that can be selected.

.. note::
   The :guilabel:`Model` is the only required field on the new vehicle form. When a model is
   selected, other fields appear on the vehicle form, and relevant information auto-populate fields
   that apply to the model. If some of the fields do not appear, this may indicate there is no model
   selected.

Driver section
--------------

This section of the vehicle form relates to the person who is currently driving the car, as well as
any plans for a change in the driver in the future, and when.

- :guilabel:`Driver`: select the driver from the drop-down menu, or type in a new driver and click
  either :guilabel:`Create "driver"` or :guilabel:`Create and edit...` to :ref:`create a new driver
  and edit the driver details <fleet/new_vehicle/add-driver>`.
- :guilabel:`Mobility Card`: if the selected driver has a mobility card listed on their employee
  card in the *Employees* application, the mobility card number appears in this field. If there is
  no mobility card listed and one should be added, :ref:`edit the employee card
  <employees/hr-settings>` in the *Employees* application.
- :guilabel:`Future Driver`: if the next driver for the vehicle is known, select the next driver
  from the drop-down menu, or type in the next driver and click either :guilabel:`Create "future
  driver"` or :guilabel:`Create and edit...` to :ref:`create a new future driver and edit the driver
  details <fleet/new_vehicle/add-driver>`.
- :guilabel:`Plan To Change Car`: if the current driver set for this vehicle plans to change their
  vehicle, either because they are waiting on a new vehicle that is being ordered, or this is a
  temporary vehicle assignment and they know which vehicle they are driving next, check this box. If
  the current driver does **not** plan to change their vehicle, do not check this box.
- :guilabel:`Assignment Date`: using the drop-down calendar, select when the vehicle is available
  for another driver. Select the date by navigating to the correct month and year using the
  :guilabel:`⬅️ (left arrow)` and :guilabel:`➡️ (right arrow)` icons, then click on the specific
  day. If this field is blank, this indicates the vehicle is currently available and can be
  reassigned to another driver. If it is populated, the vehicle is not be available to assign to
  another driver until the selected date.

.. important::
   A driver does **not** have to be an employee. All drivers are stored within the *Fleet*
   application, and if the *Contacts* application is installed, they are also stored there.

   When creating a new driver, the driver is added to both the *Fleet* application and the
   *Contacts* application, **not** the *Employees* application.

   If the *Contacts* application is not installed when a driver is added, the data is stored within
   the *Fleet* application. Upon installation of the *Contacts* application, all drivers created in
   the *Fleet* application are visible in the *Contacts* application.

.. _fleet/new_vehicle/add-driver:

Create a new driver
~~~~~~~~~~~~~~~~~~~

If a driver is not already in the system, the new driver should first be configured and added to the
database. A new driver can be added either from the :guilabel:`Driver` or :guilabel:`Future Driver`
fields on the :ref:`vehicle form <fleet/new_vehicle/vehicle-form>`.

First, type in the name of the new driver in either the :guilabel:`Driver` or :guilabel:`Future
Driver` field, then click :guilabel:`Create and edit...`. A :guilabel:`Create Driver` or
:guilabel:`Create Future Driver` form appears, depending on which field initiated the form.

Both the :guilabel:`Create Driver` and :guilabel:`Create Future Driver` forms are identical.

.. _fleet/new_vehicle/general-info:

.. note::
   Depending on what other applicaitons are installed, different, or additional tabs and/or fields
   may be visible on the :guilabel:`Create Driver` and :guilabel:`Create Future Driver` forms.

General information
*******************

Fill out the following information on the top-half of the form:

- :guilabel:`Individual` or :guilabel:`Company`: select if the driver being added is an individual
  driver or a company. Click the radio button to make a selection.

  When a selection is made, some fields may not appear on the form. If any of the fields below are
  not visible, that is because :guilabel:`Company` was selected instead of :guilabel:`Individual`.
- :guilabel:`Name`: enter a name for the driver or company in this field.
- :guilabel:`Contact`: enter the contact information in this section.

  The :guilabel:`Contact` field can be changed to a different type of contact. Click on
  :guilabel:`Contact` to reveal a drop-down menu. The available options to select are
  :guilabel:`Contact`, :guilabel:`Invoice Address`, :guilabel:`Delivery Address`,
  :guilabel:`Follow-up Address`, or :guilabel:`Other Address`.

  If desired, select one of these other options for the :guilabel:`Contact` field, and enter the
  corresponding information.

  .. note::
     If :guilabel:`Company` is selected for the  :guilabel:`Individual` or :guilabel:`Company`
     field, this field is labeled :guilabel:`Address` and cannot be modified.

- :guilabel:`Tax ID`: enter the driver or company's tax ID in this field.
- :guilabel:`Job Position`: enter the driver's job position in this field. If :guilabel:`Company` is
  selected for the :guilabel:`Individual` or :guilabel:`Company` field, this field does not appear.
- :guilabel:`Phone`: enter the driver or company's phone number in this field.
- :guilabel:`Mobile`: enter the driver or company's mobile number in this field.
- :guilabel:`Email`: enter the driver or company's email address in this field.
- :guilabel:`Website`: enter the driver or company's website address in this field.
- :guilabel:`Title`: using the drop-down menu, select the driver's title in this field. The default
  options are :guilabel:`Doctor`, :guilabel:`Madam`, :guilabel:`Miss`, :guilabel:`Mister`, and
  :guilabel:`Professor`.

  If :guilabel:`Company` is selected for the :guilabel:`Individual` or :guilabel:`Company` field,
  this field does not appear.
- :guilabel:`Tags`: using the drop-down menu, select any tags that apply to the driver or company.

  To add a new tag, type in the tag, then click :guilabel:`Create "tag"`.

  There is no limit to the number of tags that can be selected.

.. image:: new_vehicle/create-driver.png
   :align: center
   :alt: The top portion of the create driver form.

Contacts & addresses tab
************************

After the top-half of the :guilabel:`Create Driver` or :guilabel:`Create Future Driver` form is
filled out, add any other contacts and addresses associated with the driver or company in this tab.

Click the :guilabel:`Add` button to add a new contact, and a :guilabel:`Create Contact` pop-up
window appears.

Enter the following information on the form:

- :guilabel:`Contact Type`: select the type of contact being added. Click the radio button next to
  the desired type. The default options are:

  - :guilabel:`Contact`: select this option to add contact details for employees of the associated
    company.
  - :guilabel:`Invoice Address`: select this option to add a preferred address for all invoices.
    When added to the form, this address is selected by default when sending an invoice to the
    associated company.
  - :guilabel:`Delivery Address`: select this option to add a preferred address for all deliveries.
    When added to the form, this address is selected by default when delivering an order that
    belongs to the associated company.
  - :guilabel:`Follow-up Address`: select this option to add a preferred address for all follow-up
    correspondence. When added to the form, this address is selected by default when sending
    reminders about overdue invoices.
  - :guilabel:`Other Address`: select this option to add any other necessary address for the
    company.

.. image:: new_vehicle/create-contact.png
   :align: center
   :alt: The create contact form with all parts filled in.

Depending on what is selected for the :guilabel:`Contact Type`, some optional fields may not be
visible. The available fields are identical to the fields in the :ref:`general information
<fleet/new_vehicle/general-info>` section of the new driver form.

Add any notes to the :guilabel:`Internal notes...` section of the form.

After all of the information is added, click either :guilabel:`Save & Close` to add the one new
contact, or :guilabel:`Save & New` to add the current contact and create another one.

As contacts are added to this tab, each contact appears in a separate box, with an icon indicating
what type of contact is listed. For example, an :guilabel:`Invoice Address` displays a dollar sign
icon, whereas a :guilabel:`Delivery Address` displays a truck icon.

   .. image:: new_vehicle/contacts-address.png
     :align: center
     :alt: The create contact form with all parts filled in.

Sales & purchase tab
********************

Enter the following sales and purchasing information for the various sections below:

Sales
^^^^^
- :guilabel:`Salesperson`: using the drop-down menu, select the person who is the main point of
  contact for sales with this driver's company.

  This person **must** be an internal user of the company, who is found in the *Employees*
  application.
- :guilabel:`Payment Terms`: using the drop-down menu, select the default payment terms. The default
  options are: :guilabel:`Immediate Payment`, :guilabel:`15 Days`, :guilabel:`21 Days`,
  :guilabel:`30 Days`, :guilabel:`45 Days`, :guilabel:`Ed of the Following Month`, :guilabel:`10
  Days after End of Next Month`, :guilabel:`30% Now, Balance 60 Days`, and :guilabel:`2/7 Net 30`.

Purchase
^^^^^^^^
- :guilabel:`Buyer`:
- :guilabel:`Payment Terms`:
- :guilabel:`1099 Box`:
- :guilabel:`Payment Method`:
- :guilabel:`Receipt Reminder`:

Fiscal Information
^^^^^^^^^^^^^^^^^^

- :guilabel:`Fiscal Position`:

Misc
^^^^

- :guilabel:`Company ID`:
- :guilabel:`Reference`:

Accounting tab
**************

Internal notes tab
******************

Partner Assignment tab
**********************

Membership tab
**************

Vehicle section
---------------

This section of the vehicle form relates to the physical vehicle, it's various properties, when it
was added, where it is located, and who is managing it.

- :guilabel:`Immatriculation Date`: select the date the vehicle is acquired using the drop-down
  calendar.
- :guilabel:`Cancellation Date`: select the date the vehicle lease will expire, or when the vehicle
  will be no longer available, using the drop-down calendar.
- :guilabel:`Chassis Number`: enter the chassis number in the field. This is known in some countries
  as the :abbr:`VIN (Vehicle Identification Number)` number.
- :guilabel:`Last Odometer`: enter the last known odometer reading in the number field. Using the
  drop-down menu next to the number field, select whether the odometer reading is in kilometers
  :guilabel:`(km)` or miles :guilabel:`(mi)`.
- :guilabel:`Fleet Manager`: select the fleet manager from the drop-down menu, or type in a new
  fleet manager and click either :guilabel:`Create` or :guilabel:`Create and Edit`.
- :guilabel:`Location`: type in the location for the vehicle in the field. The most common scenario
  for when this field would be populated is if a company has several office locations. The typical
  office location where the vehicle is located would be the location entered.
- :guilabel:`Company`: select the company that the vehicle will be used for and associated with from
  the drop-down menu, or type in a new company and click either :guilabel:`Create` or
  :guilabel:`Create and Edit`.

.. important::
   Creating a new company may cause a subscription price change depending on the current plan. Refer
   to `Odoo's pricing plan <https://www.odoo.com/pricing-plan>`_ for more details.

.. image:: new_vehicle/new-vehicle-type.png
   :align: center
   :alt: The new vehicle form, showing the vehicle tax section.

Tax info tab
------------

Fiscality
~~~~~~~~~

- :guilabel:`Horsepower Taxation`: enter the amount that is taxed based on the size of the vehicles
  engine. This is determined by local taxes and regulations, and varies depending on the location.
  It is recommended to check with the accounting department to ensure this value is correct.
- :guilabel:`Disallowed Expense Rate`: this is the amount of non-deductible expenses for the
  vehicle. This amount is not counted towards any deductions on a tax return or as an allowable
  expense when calculating taxable income. It is recommended to check with the accounting department
  to ensure the value(s) entered are correct.

  - :guilabel:`Start Date`: enter the :guilabel:`Start Date` and :guilabel:`(%) Percentage` for when
    the :guilabel:`Disallowed Expense Rate` value goes into effect. Click :guilabel:`Add a line` to
    enter a date. Click on the blank line to display a calendar. Select the date by navigating to
    the correct month and year using the :guilabel:`⬅️ (left arrow)` and :guilabel:`➡️ (right
    arrow)` icons, then click on the specific day. Enter the percentage that is disallowed in the
    :guilabel:`% (percent)` field to the right of the date. The percentage should be entered in an
    XX.XX format. Repeat this for all entries needed.

Contract
~~~~~~~~

- :guilabel:`First Contract Date`: select the start date for the vehicle's first contract using the
  drop-down calendar. Typically this is the day the vehicle is purchased or leased.
- :guilabel:`Catalog Value (VAT Incl.)`: enter the MSRP (Manufacturer's Suggested Retail Price) for
  the vehicle at the time of purchase or lease.
- :guilabel:`Purchase Value`: enter the purchase price or the value of the lease for the vehicle.
- :guilabel:`Residual Value`: enter the current value of the vehicle.

.. note::
   The values listed above will affect the accounting department. It is recommended to check with
   the accounting department for more information and/or assistance with these values.

.. image:: new_vehicle/new-vehicle-tax.png
   :align: center
   :alt: The new vehicle form, showing the vehicle tax section.

Model tab
---------

If the model for the new vehicle is already configured in the database, the :guilabel:`Model` tab
will be populated with the corresponding information. If the model is not already in the database
and the :guilabel:`Model` tab needs to be configured, :ref:`configure the new vehicle model
<fleet/configuration/add-model>`.

Check the information in the :guilabel:`Model` tab to ensure it is accurate. For example, the color
of the vehicle, or whether there is a trailer hitch installed or not, are examples of information
that may need updating.

.. image:: new_vehicle/model-tab.png
   :align: center
   :alt: The new vehicle form, showing the vehicle tax section.

Note tab
--------

Enter any notes for the vehicle in this section.
