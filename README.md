<div align="center">

<img src="img/bckgrnd.png" alt="logo" height="auto" />

<!-- ![Views](https://komarev.com/ghpvc/?username=ivnvxd&style=flat-square) -->

<!-- [![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=flat-square&logo=facebook&logoColor=white)](https://www.facebook.com/andrey.ivanov.194)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abivanov/)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://t.me/venyxd)
[![Gmail Badge](https://img.shields.io/badge/-Gmail-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:ivnvxd@gmail.com)](mailto:ivnvxd@gmail.com) -->

</div>

```python
#!/usr/bin/env python3


class Developer(Person):

    def __init__(self):
        self.name = 'Andrey'
        self.role = 'Software Engineer'
        self.languages = ['ru-RU', 'en-US', 'de-DE']
        self.skills = ['Python', 'Django', 'Flask', 'SQL', 'HTML/CSS']
        self.tools = ['Git', 'PostgreSQL', 'Redis', 'Docker', 'Pytest', 'Bootstrap']

    def introduce(self) -> str:
        intro = f"Hello world! I'm {self.name}. \n"
        intro += f"A passionate {self.skills[0]} developer with expertise in {', '.join(self.skills)}. \n"
        intro += f"Using: {', '.join(self.tools)}."
        return intro


me = Developer()
print(me.introduce())
```

<!-- https://github.com/devicons/devicon -->
<!-- <div align="center">
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/python/python-original.svg" title="Python" alt="Python" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/django/django-plain.svg" title="Django" alt="Django" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/flask/flask-original.svg" title="Flask" alt="Flask" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/html5/html5-original.svg" title="HTML" alt="HTML" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/css3/css3-original.svg" title="CSS" alt="CSS" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/postgresql/postgresql-original.svg" title="PostgreSQL" alt="PostgreSQL" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/redis/redis-original.svg" title="Redis" alt="Redis" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/pytest/pytest-original.svg" title="Pytest" alt="Pytest" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/git/git-original.svg" title="Git" alt="Git" width="40" height="40"/>&nbsp;
    <img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/docker/docker-original.svg" title="Docker" alt="Docker" width="40" height="40"/>&nbsp;
</div> -->
