* ICE(Individual Conditional Expectation) plot
    * ice plot image <br> <img src="https://velog.velcdn.com/images%2Fkiki_%2Fpost%2F5cd4e358-f27d-49f9-9ccf-0b1e02241c91%2Fimage.png" width="200" height="150"> <br>
    * PDP plot과 전체적으로 유사하나, PDP plot과 구현 방법 중에서 각 샘플들의 예측값들을 평균내지 않고 그대로 시각화를 진행함
    * PDP에서는 알 수 없었던 feature 간 교호작용을 파악할 수 있음
    * 주의할 점
        * 샘플 수가 많거나 변수의 카디널리티가 클 때 연산량이 많아짐
            * 연산량 뿐만 아니라 시각화가 너무 더러워짐
        * 변수 간 상관성이 높을 때 비정상적인 샘플이 생성될 수 있음