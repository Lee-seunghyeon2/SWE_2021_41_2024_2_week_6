# SWE_2021_41_2024_2_week_6
---
## WeeK 4 Assignment
* Link of your repository
>[Github](https://github.com/Lee-seunghyeon2/-SWE_2021_41_2024_2_week_4/blob/main/2021310999_%EC%9D%B4%EC%8A%B9%ED%98%84%20(5).ipynb)  
</pre>

```python
def isHappy(n):

    thisset = set()

    while n not in thisset:
        thisset.add(n)
        number = []
        while n != 0:
            temp = n % 10
            number.append(temp*temp)
            n //= 10

        if sum(number) == 1:
            return True
        else:
            n = sum(number)

    return False

    return

print(isHappy(int(input())))
```
* Description of your code
---
## Week 5 Assignment


</pre>

>```python  
>docker exec <your container> cat /etc/os-release 
>``` 
>* Explanation of commaindline and your ouptut

</pre>  

>```python   
>docker exec <your container> git --version
>```
>* Explanation of commaindline and your ouptut

</pre>

>```python   
>docker exec <your container> python3 --version
>```
>* Explanation of commaindline and your ouptut

</pre>

>```python   
>docker inspect --format="{{ .HostConfig.Binds }}" <container_name>
>```
>* Explanation of commaindline and your ouptut
