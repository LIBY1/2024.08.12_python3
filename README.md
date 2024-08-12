# 2024.08.12_python3

# 사용자로부터 숫자를 입력받기
user_input = input("숫자를 입력하세요: ")

# 입력된 값을 정수로 변환
try:
    number = int(user_input)
    
    # 짝수인지 홀수인지 확인
    if number % 2 == 0:
        print(f"{number}은(는) 짝수입니다.")
    else:
        print(f"{number}은(는) 홀수입니다.")
except ValueError:
    print("유효한 숫자를 입력해 주세요.")










