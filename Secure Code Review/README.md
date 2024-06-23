# Source Code Review 

What is Source Code Review?
>A secure code review is a line-by-line analysis of the source code of an application, usually performed to find any security risks overlooked during the pre or post-development phase. A secure code review aims to analyze an application's source code and determine whether it has any security vulnerabilities or flaws.

---

### Awesome Resouces:
| Credit                                                      | Link                                                                  |
|-------------------------------------------------------------|-----------------------------------------------------------------------|
| [Cobalt.io](https://www.cobalt.io/blog/a-pentesters-guide-to-source-code-review)               | [A Pentester's Guide to Source Code Review](https://www.cobalt.io/blog/a-pentesters-guide-to-source-code-review)   |
| [Cobalt.io](https://www.cobalt.io/blog/source-code-review)               | [Source Code Review](https://www.cobalt.io/blog/source-code-review)   |
| [@prasad508](https://medium.com/@prasad508/how-to-series-source-code-review-part-1-458b3a8d9569)             | [How to Series: Source Code Review Part 1](https://medium.com/@prasad508/how-to-series-source-code-review-part-1-458b3a8d9569) |
| [codegrip.tech ](https://www.codegrip.tech/productivity/best-practices-for-reviewing-code/)          | [Best Practices for Reviewing Code](https://www.codegrip.tech/productivity/best-practices-for-reviewing-code/) |
| [YouTube - @HackerVlog ](https://www.youtube.com/watch?v=MSM1_y8Ih3A)          | [Video 1](https://www.youtube.com/watch?v=MSM1_y8Ih3A) |
| [YouTube - @hackervloglive](https://www.youtube.com/watch?v=Ft-1hjns0-Y)          | [Video 2](https://www.youtube.com/watch?v=Ft-1hjns0-Y) |
| [YouTube - @HackerVlog](https://www.youtube.com/watch?v=YlhDmJyQEGk)          | [Video 3](https://www.youtube.com/watch?v=YlhDmJyQEGk) |


---
**Common Tools Free and Paid:**
| Open Source Tools                                                                          | Source Code Review Commercial                                                                       |
| ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| [SonarQube Download](https://sonarqube.org/downloads)                                      | [Checkmarx Static Application Security Testing (SAST)](https://www.checkmarx.com/)                  |
| [Semgrep Download](https://semgrep.dev/docs/introduction/installation)                     | [AppScan Source - HCL](https://www.hcltechsw.com/wps/portal/products/appscan)                       |
| [Snyk Download](https://snyk.io/docs/getting-started/install-cli/)                         | [Fortify](https://www.microfocus.com/en-us/cyberres/application-security/static-code-analysis-sast) |
| [Betterscan-ce Download](https://github.com/checkmarx-ltd/better-scan)                     | [Klocwork](https://www.roguewave.com/products/klocwork)                                             |
| [VCG - VisualCodeGrepper](https://github.com/Arachni/arachni/wiki/VCG---VisualCodeGrepper) | [Veracode](https://www.veracode.com/)                                                               |
| [Yasca - Yet Another Source Code Analyzer](https://github.com/scovetta/yasca)              |                                                                                                     |
| [Findbugs](https://find-sec-bugs.github.io/)                                               |                                                                                                     |
| [RIPS Scanner](https://www.ripstech.com/download/)                                         |                                                                                                     |
| [OWASP Orizon](https://owasp.org/www-project-orizon/)                                      |                                                                                                     |
| [LAPSE](https://github.com/sourceclear/lapse)                                              |                                                                                                     |
| [FxCOP](https://github.com/dotnet/roslyn-analyzers)                                        |                                                                                                     |
| [RATS](https://github.com/andlabs/rats)                                                    |                                                                                                     |
| [Raptor Download](https://github.com/viper-framework/raptor)                               |                                                                                                     |




---
# Code Review Checklist

| Credits | https://github.com/mgreiler | [awesomecodereviews.com](https://www.awesomecodereviews.com/) |
| ------- | --------------------------- | ------------------------------------------------------------- |
|         |                             |                                                               |

## Implementation
- [ ] Does this code change accomplish what it is supposed to do?
- [ ] Can this solution be simplified?
- [ ] Does this change add unwanted compile-time or run-time dependencies?
- [ ] Is a framework, API, library, or service used that should not be used?
- [ ] Could an additional framework, API, library, or service improve the solution?
- [ ] Is the code at the right abstraction level?
- [ ] Is the code modular enough?
- [ ] Can a better solution be found in terms of maintainability, readability, performance, or security?
- [ ] Does similar functionality already exist in the codebase? If yes, why isn’t it reused?
- [ ] Are there any best practices, design patterns or language-specific patterns that could substantially improve this code? 
- [ ] Does this code adhere to Object-Oriented Analysis and Design Principles, like the Single Responsibility Principle, Open-Close Principle, Liskov Substitution Principle, Interface Segregation, or Dependency Injection?

## Logic Errors and Bugs
- [ ] Can you think of any use case in which the
code does not behave as intended?
- [ ] Can you think of any inputs or external events
that could break the code?

## Error Handling and Logging
- [ ] Is error handling done the correct way?
- [ ] Should any logging or debugging information
be added or removed?
- [ ] Are error messages user-friendly?
- [ ] Are there enough log events and are they
written in a way that allows for easy
debugging?

## Dependencies
- [ ] Were updates to documentation, configuration, or readme files made as required by this change?
- [ ] Are there any potential impacts on other parts of the system or backward compatibility?

## Security and Data Privacy
- [ ] Does the code introduce any security vulnerabilities?
- [ ] Are authorization and authentication handled correctly?
- [ ] Is (user) input validated, sanitized, and escaped 
to prevent security attacks such as cross-site 
scripting or SQL injection?
- [ ] Is sensitive data like user data or credit card
information securely handled and stored?
- [ ] Is the right encryption used?
- [ ] Does this code change reveal any secret
information like keys, passwords, or usernames?
- [ ] Is data retrieved from external APIs or libraries
checked for security issues?

## Performance
- [ ] Do you think this code change decreases
system performance?
- [ ] Do you see any potential to improve the
performance of the code significantly?


## Usability and Accessibility
- [ ] Is the proposed solution well-designed from a
usability perspective?
- [ ] Is the API well documented?
- [ ] Is the proposed solution (UI) accessible?
- [ ] Is the API/UI intuitive to use?

## Ethics and Morality
- [ ] Does this change make use of user data in a way that 
might raise privacy concerns?
- [ ] Does the change exploit behavioral patterns or human
weaknesses? 
- [ ] Might the code, or what it enables, lead to mental 
and physical harm for (some) users?
- [ ] If the code adds or alters ways in which people 
interact with each other, are appropriate measures
in place to prevent/limit/report harassment or abuse?
- [ ] Does this change lead to an exclusion of a certain
group of people or users?
- [ ] Does this code change introduce unjust impact on people, 
particularly those related to sensitive characteristics such as
race, ethnicity, gender, nationality, income, sexual orientation, ability, 
and political or religious belief?
- [ ] Does this code change introduce any algorithm, 
AI  or machine learning bias?


## Testing and Testability
- [ ] Is the code testable?
- [ ] Has the code change
- [ ] Have automated tests been added, or have related ones been updated to cover the change?
- [ ] Do the existing tests reasonably cover the code change (unit/integration/system tests)? 
- [ ] Are there some test cases, input or edge cases
that should be tested in addition?

## Readability
- [ ] Is the code easy to understand?
- [ ] Which parts were confusing to you and why?
- [ ] Can the readability of the code be improved by
smaller methods?
- [ ] Can the readability of the code be improved by
different function, method or variable names?
- [ ] Is the code located in the right
file/folder/package?
- [ ] Do you think certain methods should be
restructured to have a more intuitive control
flow?
- [ ] Is the data flow understandable?
- [ ] Are there redundant or outdated comments?
- [ ] Could some comments convey the message
better?
- [ ] Would more comments make the code more
understandable?
- [ ] Could some comments be removed by making the code itself more readable?
- [ ] Is there any commented-out code?

## Experts' Opinion
- [ ] Do you think a specific expert, like a security
expert or a usability expert, should look over
the code before it can be accepted?
- [ ] Will this code change impact different teams, and should they review the change as well?



