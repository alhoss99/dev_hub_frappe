# Doc. Event | In frappe server side
    before_insert
    after_insert
    before_validate
    validate
    on_update
    on_change
    on_submit
    before_cancel
    on_cancel
    on_trash
    after_delete
    before_update_after_submit
    on_update_after_submit
    before_print


## 1

```python
    def before_insert(self):
        """
        trigger before Insert the document in the database (as a new document).
        this will not trigger for existing records.
		This will check for user permissions if ignore_permissions flag is false
        """
        pass
```
 ## 2
```python    
    def after_insert(self):
        """
        trigger after Insert the document in the database (as a new document).
        this will not trigger for existing records.
        """
        pass
```        
## 3
```python    
    def before_validate(self):
        """
        method should be executed before ignoring validations.
        this will execute for both save and submit
        """
```        
## 4
```python    
    def validate(self):
        """
        this will trigger before_save ----  for save action
        this will trigger before_submit ---- for submit action
        This will check for user permissions if ignore_permissions flag is false
        """
```        
## 5
```python    
    def on_update(self):
        """
        this will trigger when doctype have any chnages
        """
```        
## 6
```python    
    def on_change(self):
        """
        this will trigger if the doctype have any workflow action
        """
```        
## 7
```python    
    def on_submit(self):
        """
        this will trigger only before submit the doctype
        This will check for user permissions if ignore_permissions flag is false
        """
```        
## 8
```python    
    def before_cancel(self):
        """
        this will trigger before canceling a submitted document.
        """
```        
        
## 9
```python    
    def on_cancel(self):
        """
        this will trigger after canceling a submitted document.
        """
        
```        
 ## 10
```python    
    def on_trash(self):
        """
        this will trigger before deleting a document.
        """  
```        
## 11
```python    
    def after_delete(self):
        """
        this will trigger after deleting a document.
        """
```        
## 12
```python    
    def before_update_after_submit(self):
        """
        this will trigger before if value changed in any allow on submit field
        """
```        
## 13
```python    
    def on_update_after_submit(self):
        """
        this will trigger after if value changed in any allow on submit field
        """
```        
## 14
```python    
    def before_print(self):
        """
        this will trigger before print preview 
        """


1. `before_insert`:
   - يُستدعى هذا الدالة قبل إدراج الوثيقة (Document) في قاعدة البيانات كوثيقة جديدة.
   - يتم التحقق من صلاحيات المستخدم إذا كانت قيمة `ignore_permissions` غير صحيحة.
   
2. `after_insert`:
   - يُستدعى هذا الدالة بعد إدراج الوثيقة في قاعدة البيانات كوثيقة جديدة.
   
3. `before_validate`:
   - يُستدعى هذا الدالة قبل تجاهل الفحوصات (validations).
   - يُنفذ سواء كانت العملية حفظًا (save) أو تقديمًا (submit).

4. `validate`:
   - يُستدعى هذا الدالة قبل الحفظ (`before_save`) في حالة الحفظ وقبل التقديم (`before_submit`) في حالة التقديم.
   - يتم التحقق من صلاحيات المستخدم إذا كانت قيمة `ignore_permissions` غير صحيحة.

5. `on_update`:
   - يُستدعى هذا الدالة عندما يتم تغيير الوثيقة.

6. `on_change`:
   - يُستدعى هذا الدالة إذا كان هناك أي إجراء في سير العمل (workflow) للوثيقة.

7. `on_submit`:
   - يُستدعى هذا الدالة قبل تقديم الوثيقة فقط.
   - يتم التحقق من صلاحيات المستخدم إذا كانت قيمة `ignore_permissions` غير صحيحة.

8. `before_cancel`:
   - يُستدعى هذا الدالة قبل إلغاء وثيقة مقدمة.

9. `on_cancel`:
   - يُستدعى هذا الدالة بعد إلغاء وثيقة مقدمة.

10. `on_trash`:
    - يُستدعى هذا الدالة قبل حذف وثيقة.

11. `after_delete`:
    - يُستدعى هذا الدالة بعد حذف وثيقة.

12. `before_update_after_submit`:
    - يُستدعى هذا الدالة قبل التحديث إذا تغيرت القيمة في أي حقل مسموح بتحديثه بعد التقديم.

13. `on_update_after_submit`:
    - يُستدعى هذا الدالة بعد التحديث إذا تغيرت القيمة في أي حقل مسموح بتحديثه بعد التقديم.

14. `before_print`:
    - يُستدعى هذا الدالة قبل معاينة الطباعة.

تُستخدم هذه الوظائف لتخصيص سلوك الوثائق ومعالجة البيانات وفقًا لاحتياجات التطبيق.
```