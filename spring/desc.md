## Spring 요청 흐름

### RequestContextHolder
ContextHolder 에서 알 수 있듯이 Context(문맥) 에 대한 정보를 (ThreadLocal) 에 보관하는 객체이다. 
ContextHolder 는 ThreadLocal과 합성 관계이다. 

'''
// 이런 식으로 하여 HttpServletRequest 객체에 접근할 수 있다.
HttpServletRequest getCurrentRequest() {
        ServletRequestAttributes attributes =
                (ServletRequestAttributes) RequestContextHolder.getRequestAttributes();

        return (attributes != null ? attributes.getRequest() : null);
}
'''

## Argument Resolver 
Spring MVC Controller의 매개변수를 전처리하는 객체이다.
Controller 단에서 매개변수에 대한 전처리 책임을 맡아 코드의 가독성과 유지보수성을 올릴 수 있다.

흔히 많이 사용하는 경우는 인증 인가 상황에서 많이 사용된다.

