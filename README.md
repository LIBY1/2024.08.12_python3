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


%pip install ultralytics opencv-python-headless matplotlib
from google.colab import files
uploaded = files.upload()
filename = next(iter(uploaded))
!mkdir -p /content/sample_data
!mv {filename} /content/sample_data/(filename)




from ultralytics import YOLO
from IPython.display import Image, display
model = YOLO('yolov8n.pt')
image_path = '/content/sample_data/1.jpg'
results = model.predict(image_path)
first_result = results[0]
first_result.save()
saved_image_path = '/content/results_1.jpg'
display(Image(saved_image_path))








