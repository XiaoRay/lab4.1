#!/usr/bin/python
# -*- coding: utf-8 -*-


from django.contrib import admin
from book.models import *

class BooksAdmin(admin.ModelAdmin):
    list_display = ('Title', 'ISBN', 'AuthorID', 'Publisher', 'Publishdate', 'Price')
    search_fields = ('Title',)
    
    ordering = ('AuthorID', )
    
    fieldsets = [('书名及编号', {'fields': ['Title', 'ISBN']}),
                 ('作者信息', {'fields': ['AuthorID']}),
                 ('出版社', {'fields': ['Publisher']}),
                 ('出版日期', {'fields': ['Publishdate']}),
                 ('价格', {'fields': ['Price']}),
                 ]    
admin.site.register(Books,BooksAdmin)



class AuthorAdmin(admin.ModelAdmin):
    list_display = ('AuthorID', 'Name', 'Age', 'Country', )
    search_fields = ('Name',)
    
    ordering = ('Name', )
   
    fieldsets = [('作者姓名', {'fields': ['Name', 'AuthorID']}),
                 ('年龄', {'fields': ['Age']}),
                 ('国籍', {'fields': ['Country']})
                ]
admin.site.register(Author,AuthorAdmin)

