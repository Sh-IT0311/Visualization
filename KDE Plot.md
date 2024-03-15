* kde(kernel density estimation) plot
    * kde plot image <br>![kde plot](https://media.geeksforgeeks.org/wp-content/uploads/20190318124445/Screenshot-564.png) <br>
    * 배경지식
        * 커널 함수(kernel function)
            * 원점을 중심으로 대칭이면서 적분값이 1이고, non-negative인 함수
            * 대표적으로 Gaussian, Epanechnikov, uniform 함수 등이 있음 
        * 밀도 추정(density estimation)
            * 머신러닝, 확률, 통계 등에서 말하는 밀도는 확률밀도를 의미함
            * 즉, 어떤 변수의 밀도를 추정하는 것은 어떤 변수의 확률밀도함수를 추정하는 것을 의미함
                * 어떤 변수의 확률밀도함수를 구할 수 있으면 그 변수가 가질 수 있는 값의 범위 및 확률분포, 특성을 모두 알 수 있기 때문에 확률밀도함수 추정은 매우 중요함
            * 추정방법
                * Parametric method
                    * 어떠한 변수가 미리 어떠한 확률밀도함수를 따른다고 가정하고 데이터로 모수(Parameter)를 추정하는 방식
                * Non-parmetric method
                    * 어떠한 가정 없이 관측된 데이터만으로 확률밀도함수를 추정하는 방식
                    * 가장 간단한 방법이 히스토그램임
                        * bin의 경계에서 불연속성이 나타는 점, bin의 크기 및 시작 위치에 따라서 히스토그램이 달라지는 문제점이 있음
                            * 이러한 문제점을 개선한 방법으로 커널함수를 누적해서 밀도추정 하게됨(-> kde)
    * 커널함수를 활용해서 밀도추정 하는 방법
    * 관측된 데이터 각각마다 해당 데이터 값을 중심으로 하는 커널 함수를 생성하고 누적해서 더하고 전체 데이터 개수로 나누어서 밀도추정을 하게 됨
        * smoothing한 histogram을 얻을 수 있음
    * 고려해야할 점
        * 어떤 커널 함수를 사용할 것인가
        * 커널함수의 bandwidth를 결정하는 파라미터 h 값을 어떻게 잡을 것인가
            * h가 작으면 뾰족하고, h가 크면 완만한 형태를 만듬
    * [참고사이트](https://darkpgmr.tistory.com/147)
    * [예시코드](https://seaborn.pydata.org/generated/seaborn.kdeplot.html)