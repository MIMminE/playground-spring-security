# Spring Security 아주 간단한 예제

이 예제는 모든 요청에 인증이 필요하고, 기본 로그인 폼을 사용하는 최소 설정입니다.

## SecurityConfig.java

```java
import org.springframework.context.annotation.Bean;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.web.SecurityFilterChain;
import org.springframework.context.annotation.Configuration;

@Configuration
public class SecurityConfig {
    @Bean
    public SecurityFilterChain filterChain(HttpSecurity http) throws Exception {
        http
            .authorizeHttpRequests((authz) -> authz
                .anyRequest().authenticated()
            )
            .formLogin(); // 기본 로그인 폼 사용
        return http.build();
    }
}
```
```

---

## 3. 마크다운에서 코드블록 쓰는 법

- 코드블록은 <code>```</code> (backtick 3개)로 감싸서 만듭니다.
- 언어를 지정하려면 <code>```java</code>처럼 backtick 뒤에 언어명을 씁니다.
- 설명은 일반 텍스트로 작성하면 됩니다.

---

## 4. 실제 결과 예시

아래처럼 보입니다:

---

# Spring Security 아주 간단한 예제

이 예제는 모든 요청에 인증이 필요하고, 기본 로그인 폼을 사용하는 최소 설정입니다.

## SecurityConfig.java

```java
import org.springframework.context.annotation.Bean;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.web.SecurityFilterChain;
import org.springframework.context.annotation.Configuration;

@Configuration
public class SecurityConfig {
    @Bean
    public SecurityFilterChain filterChain(HttpSecurity http) throws Exception {
        http
            .authorizeHttpRequests((authz) -> authz
                .anyRequest().authenticated()
            )
            .formLogin(); // 기본 로그인 폼 사용
        return http.build();
    }
}
```

---

이런 식으로 마크다운 파일을 작성하시면 됩니다!  
궁금한 점 있으면 언제든 질문해 주세요.