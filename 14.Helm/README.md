# Helm

### Goals
- The trainee will get familiar with Helm and Helm Charts

### Tasks
- What is helm and what is it used for?
- What is a Helm chart's directory structure?
- What is Chart.yaml?
- What are the benefits of using Helm Charts?
- What templating language is Helm using?
- How can you customize a helm chart?
- What is the '.'?
- What special values do you have access to when templating?
- What are named templates?
- what is _helpers.tpl file? Why does it start with an underscore?
- What effect does the "{{-" simbol has on your template?
- What are subcharts?
- How can I control values passed to a subchart?
- What effect do variables under `.Values.global` have?
- How can I use two value files with helm cli?
- Read the helm docs about conventions and best practices


### Exerise 
- Install helm cli tool and experiment with helm
- Use helm cli to create a helm chart and see what it looks like
- Create a helm chart which uses some bitnami helm chart as a dependency
- What is the equivalent single value file to using these two files (helm template --values A.values.yaml --values B.values.yaml )? Try working it out and write it before checking with helm.   
    #### A.values.yaml
    ```yaml
    yoav:
      instrument: piano
      address: frishman
      hobbies:
        - 'riding bike'
        - 'playing music'
        - knives
      favoriteFood: 'lint 90% dark chocolate'
    notebookClosed: true
    ```
    #### B.values.yaml
    ```yaml
    yoav:
      nickName: yoavi
      hobbies:
        - 'riding bike'
        - 'walking bare foot'
        - 'getting released' 
      favoriteFood: hada
    notebookClosed: false
    guitarCount: 2
    ``` 
<br>

---

## 2nd Exercise
- Check out some of the helm charts in our tactic environment.  
- Refer to the official [Helm documentation](https://helm.sh/docs/) to better understand chart structure and syntax.