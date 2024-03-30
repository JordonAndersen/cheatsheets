## Django Models and Validations Cheat Sheet

This cheat sheet provides a quick reference for working with models and validations in Django projects.

**Models:**

* **Define models in `models.py`:** Create classes representing your data structure.
* **Fields:** Use Django field types like `CharField`, `IntegerField`, `BooleanField`, `DateField`, etc. to define data types.
* **Relationships:** Use fields like `ForeignKey` and `ManyToManyField` to establish relationships between models (one-to-one, one-to-many, many-to-many).
* **`Meta` class (optional):** Use `Meta` to configure model behavior (e.g., `db_table` for custom database table name).

**Example:**

```
from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=255)
    author = models.ForeignKey(Author, on_delete=models.CASCADE)
    publication_date = models.DateField()

class Author(models.Model):
    name = models.CharField(max_length=100)
```

**Validations:**

* **Field-level validations:**
   - Use field attributes like `max_length`, `unique=True`, `null=True`, `blank=True` to define constraints.
   - Use validators (e.g., `EmailValidator()`) for specialized validation.
* **Method-level validations (clean methods):**
   - Define methods starting with `clean_` (e.g., `clean_title()`) to perform custom validation logic.
   - Raise `ValidationError` to indicate errors with specific messages.

**Example:**

```
class Book(models.Model):
    title = models.CharField(max_length=255, validators=[EmailValidator()])

    def clean_title(self):
        if "badword" in self.title.lower():
            raise ValidationError("Title cannot contain 'badword'")
```

**Additional Tips:**

* Use built-in Django validators (e.g., `EmailValidator()`, `URLValidator()`) for common validation needs.
* Consider using third-party libraries like `django-crispy-forms` for easier form validation integration.
* Test your validations thoroughly to ensure data integrity.

**Resources:**

* Django Models: [https://docs.djangoproject.com/en/5.0/](https://docs.djangoproject.com/en/5.0/)
* Django Validations: [https://docs.djangoproject.com/en/5.0/](https://docs.djangoproject.com/en/5.0/)
