```python
#!/usr/bin/env python3


class Person:
    
    def __init__(self):
        self.name = 'Andrey'
        self.languages = ['ru-RU', 'en-US', 'de-DE']


class SoftwareEngineer(Person):
    
    def __init__(self):
        super().__init__()
        self.role = 'Python developer'
        self.skills = {
            'code': ['Python', 'SQL', 'HTML', 'CSS'],
            'tools': ['Django', 'Flask', 'PostgreSQL', 'Redis', 'Docker', 'Git' 'Pytest', 'Bootstrap']
        }

    def introduce(self):
        intro = f"Hello world! I'm {self.name}. \n"
        intro += f"Passionate {self.role} with product management & entrepreneurship background."
        print(intro)


me = SoftwareEngineer()
me.introduce()

# I love to connect with different people, so feel free to reach out to me!
```
