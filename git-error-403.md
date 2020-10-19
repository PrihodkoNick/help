​	Была такая ошибка при попытке запушить в удаленный репозиторий

> При git push вылазит ошибка:
> remote: Permission to someSite.git denied to Barzini.
> fatal: unable to access 'https://github.com/somesute.git/': The requested URL returned error: 403 

**Решение:**

​	Была такая же проблема в винде - сменил аккаунт на гитхабе, но при пуше гит упорно пытался законнектиться по старому логину. Вылечил вот так:

- git config --global credential.github.com.interactive **always**
- теперь пушим и вводим новые логин/пароль
- git config --global credential.github.com.interactive **auto** - возвращаем значение по умолчанию