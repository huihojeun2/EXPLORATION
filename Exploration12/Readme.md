# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 전휘호, 이재영
- 리뷰어 : 강다은


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
    - 문제를 해결하는 완성된 코드란 프로젝트 루브릭 3개 중 2개, 
    퀘스트 문제 요구조건 등을 지칭
        - 해당 조건을 만족하는 코드를 캡쳐해 근거로 첨부
     
        <br/>
     
        > 학습 모델을 이용하여 abstrative summarization, extractive summarization 을 성공적으로 수행하고 비교히보았습니다

        ```
        원문 : taiwan thursday said deeply disappointed state owned national carrier air india changed taiwan chinese official website described pressure china external affair ministry however defended decision saying change consistent international norm india policy island 
        실제 요약 : ai chinese 
        예측 요약 :  india u official
        ```

        ```
        Original : 
         Former Finance Minister Yashwant Sinha on Tuesday demanded a probe into the alleged diversion of loans worth â‚¹31,000 crore by Dewan Housing Finance (DHFL). All agencies including regulators of the government have failed to track nefarious deals, he said. This comes after a media report on Tuesday accused DHFL's controlling shareholders of diverting funds to shell companies to buy assets.
        
        Summarized text: 
         Former Finance Minister Yashwant Sinha on Tuesday demanded a probe into the alleged diversion of loans worth â‚¹31,000 crore by Dewan Housing Finance (DHFL). 
        ```
     
        ```
        추상적 요약은 핵심 단어만 추출해오니 핵심적인 부분을 빠르게 볼 수 있다.
        추출적 요약은 불용어 부분을 삭제하지 않아 문장이 조금 더 자연스러운 경향이 있다.
        ```

        <br/>
    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
     
        <br/>
     
        > 변수 선언 또는 함수 호출 시 그 역할과 과정을 주석을 통해 잘 설명하였습니다
        
        ```
        #등장 빈도수가 7회 미만인 단어들이 데이터에서 얼만큼의 비중을 차지하는지 확인

        threshold = 7
        total_cnt = len(src_tokenizer.word_index) # 단어의 수
        rare_cnt = 0 # 등장 빈도수가 threshold보다 작은 단어의 개수를 카운트
        total_freq = 0 # 훈련 데이터의 전체 단어 빈도수 총 합
        rare_freq = 0 # 등장 빈도수가 threshold보다 작은 단어의 등장 빈도수의 총 합
        
        # 단어와 빈도수의 쌍(pair)을 key와 value로 받는다.
        for key, value in src_tokenizer.word_counts.items():
            total_freq = total_freq + value
        
            # 단어의 등장 빈도수가 threshold보다 작으면
            if(value < threshold):
                rare_cnt = rare_cnt + 1
                rare_freq = rare_freq + value
        ```
        <br/>
        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
     
        <br/>
     
        > 학습에 활용되는 데이터의 길이와 단어 갯수의 기준을 정하기 위해, 꼼꼼한 실험을 통해 데이터를 분석하였습니다
        
        ```
        print('전체 샘플 중 길이가 %s 이하인 샘플의 비율: %s'%(max_len, (cnt / len(nested_list))))
        ```
        
        ```
        print('단어 집합(vocabulary)의 크기 :', total_cnt)
        print('등장 빈도가 %s번 이하인 희귀 단어의 수: %s'%(threshold - 1, rare_cnt))
        print('단어 집합에서 희귀 단어를 제외시킬 경우의 단어 집합의 크기 %s'%(total_cnt - rare_cnt))
        print("단어 집합에서 희귀 단어의 비율:", (rare_cnt / total_cnt)*100)
        print("전체 등장 빈도에서 희귀 단어 등장 빈도 비율:", (rare_freq / total_freq)*100)
        ```
        <br/>
        
- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
     
        <br/>
     
        > 회고록을 통해서 데이터 전처리의 어려움과 고민해야 할 방향에 대하여 제시하였습니다
     
        ```
        코드를 돌리는데 전처리 부분이 너무 오래걸렸다...
        이건 어쩔 수 없는 부분인거 같다
        데이터 전처리를 하는데 표제어 처리라는 전처리 방법이 있길래 한번 사용해보니 val loss값이 줄었다.
        다양한 데이터 전처리 방법을 추가해봤지만 성능이 좋아지는 방식도 있고 좋아지지 않은 방식도 있어서 상황에 따라 잘 판단하고 사용해야 될거같다.
        그리고 이상치를 판단해서 샘플을 남기는 부분도 이상치를 그대로 제거해버리면 다른 데이터와 달리 텍스트 데이터는 학습에 부정적인 영향을 미칠 수도 있을거 같아서 샘플 제거 부분에 대해서 신중해야 될거같다.
        ```

        <br/>
        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 하드코딩을 하지않고 함수화, 모듈화가 가능한 부분은 함수를 만들거나 클래스로 짰는지
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화했는지
        - 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부합니다.
     
        <br/>
     
        > 자주 사용하는 기능의 코드나 비슷한 기능을 하는 코드를 묶어서 함수화하였습니다. 변수명, 함수명 또한 파이썬 스타일 가이드에 맞게 명확하고 간결하게 정의하였습니다.
        
        ```
        # 데이터 전처리 함수
        def preprocess_sentence(sentence, remove_stopwords=True):
            sentence = sentence.lower() # 텍스트 소문자화
            sentence = BeautifulSoup(sentence, "lxml").text # <br />, <a href = ...> 등의 html 태그 제거
            sentence = re.sub(r'\([^)]*\)', '', sentence) # 괄호로 닫힌 문자열 (...) 제거 Ex) my husband (and myself!) for => my husband for
            sentence = re.sub('"','', sentence) # 쌍따옴표 " 제거
            sentence = ' '.join([contractions[t] if t in contractions else t for t in sentence.split(" ")]) # 약어 정규화
            sentence = re.sub(r"'s\b","", sentence) # 소유격 제거. Ex) roland's -> roland
            sentence = re.sub("[^a-zA-Z]", " ", sentence) # 영어 외 문자(숫자, 특수문자 등) 공백으로 변환
            sentence = re.sub('[m]{2,}', 'mm', sentence) # m이 3개 이상이면 2개로 변경. Ex) ummmmmmm yeah -> umm yeah
            lemmatizer = WordNetLemmatizer() # 표제어 추출
            
            # 불용어 제거 (Text)
            if remove_stopwords:
                tokens = ' '.join(lemmatizer.lemmatize(word) for word in sentence.split() if not word in stopwords.words('english') if len(word) > 1)
            # 불용어 미제거 (Summary)
            else:
                tokens = ' '.join(lemmatizer.lemmatize(word) for word in sentence.split() if len(word) > 1)
            return tokens
        ```
        <br/>
        <br/>


# 참고 링크 및 코드 개선
```
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```

**친절하신 휘호님께**  
코드 리뷰 너무 즐거웠습니다 😁ㅎㅎㅎ  
본의아니게 리뷰가 조금 늦어졌는데 양해해주셔서 감사합니다  
회고록에 남겨주신 데이터 전처리에 관한 고민 내용은 저도 공감하면서 잘 읽어보았습니다  
자연어의 세계는 정말 알쏭달쏭한 것 같아요 😗💦
