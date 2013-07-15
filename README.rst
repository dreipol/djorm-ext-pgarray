djorm-ext-pgarray
=================

PostgreSQL native array fields extension for Django.


ArrayFormField
--------------

If you're using a ArrayFormField with for a special type you can write a converter for the items:

Example in admin.py:

int_converter = lambda strng: int(strng)

class ExampleModelForm(ModelForm):
    activity = ArrayFormField(convert_with=int_converter)
	...