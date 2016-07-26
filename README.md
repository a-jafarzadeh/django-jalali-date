# django-jalali-date
Jalali Date support for user interface. Easy conversion of DateTimeFiled to JalaliDateTimeField within the admin site.

----------
**DEPENDENCY**

To use this module you need to install jdatetime(and of course you need django) module which you can install it with easy_install or pip

----------
**INSTALL**

    pip install django-jalali-date   

----------
**USAGE**

settings.py

    INSTALLED_APPS = [
	    ...
	    'jalali_date',
	    ...
	]
admin.py

	from django.contrib import admin
	from jalali_date import admin as j_admin
	
    
    class MyInlines1(j_admin.TabularInline):
	    model = SecendModel
    
    class MyInlines2(j_admin.StackedInline):
	    model = ThirdModel
	
	@admin.register(FirstModel)
	class FirstModelAdmin(j_admin.ModelAdmin):
		inlines = (MyInlines1, MyInlines2, )    

![enter image description here](https://drive.google.com/open?id=0BxfgUeJSa39vQno0ZjZMNmplOTg)