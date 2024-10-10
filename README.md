# SWE_2021_41_2024_2_week_6
---
## WeeK 4 Assignment
* Link of your repository    [Github](https://github.com/Lee-seunghyeon2/-SWE_2021_41_2024_2_week_4/blob/main/2021310999_%EC%9D%B4%EC%8A%B9%ED%98%84%20(5).ipynb)  
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
  ishappy()는 입력받은 숫자가 happy num인지 확인하는 함수이다. 이때 happy num은 각 자리수의 제곱의 합을 구하고, 다시 그 합을 입력받는 값으로 사용하여, 결과값이 1이 나올 수 있는 수이다. 
---
## Week 5 Assignment


</pre>

>```python  
>docker exec ubuntu-container cat /etc/os-release 
>``` 
>* Explanation of commaindline and your ouptut
>* output:
>> PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
>>LOGO=ubuntu-logo
>* Explanation: 실행중인 docker container에서 cat 명령어를 사용하여 /etc/os-release 내용을 출력한다.
이때 container의 이름은 ubuntu-container이다.

</pre>  

>```python   
>docker exec ubuntu-container git --version
>```
>* Explanation of commaindline and your ouptut
>* output: git version 2.43.0
>* Explanation: 실행중인 docker container에서 git의 설치 여부와 버젼 정보를 출력한다.
이때 container의 이름은 ubuntu-container이다.

</pre>

>```python   
>docker exec ubuntu-container python3 --version
>```
>* Explanation of commaindline and your ouptut
>* output: Python 3.12.3
>* Explanation: 실행중인 docker container에서 python의 설치 여부와 버젼 정보를 출력한다.
이때 container의 이름은 ubuntu-container이다.

</pre>

>```python   
>docker inspect --format="{{ .HostConfig.Binds }}" ubuntu-container
>```
>* Explanation of commaindline and your ouptut
>* output: [./ossp_host_dir:/mnt/ubuntu-container_dir]
>* Explanation: docker inspect을 통하여 docker container의 정보를 확인한다.
이때 확인할 정보는 .HostConfig.Binds이며 container 이름은 ubuntu-container이다.
결과로 host 디렉토리와 container 디렉토리에서 마운트된 디렉토리를 보여준다.
