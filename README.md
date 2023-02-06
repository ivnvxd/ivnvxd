```python
#!/usr/bin/env python3


class Person:

    def __init__(self):
        self.name = 'Andrey'
        self.languages = ['ru-RU', 'en-US', 'de-DE']


class Developer(Person):

    def __init__(self):
        self.role = 'Software Engineer'
        self.skills = {
            'code': ['Python', 'SQL', 'HTML', 'CSS'],
            'tools': ['Django', 'Flask', 'Git', 'PostgreSQL', 'Redis', 'Docker', 'Pytest', 'Bootstrap']
        }

        super().__init__()

    def introduce(self):
        intro = f"Hello world! I'm {self.name}. \n"
        intro += f"Passionate {self.skills['code'][0]} developer with product management & entrepreneurship background."
        print(intro)


me = Developer()
me.introduce()
```
