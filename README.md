# jsx_tips_talk

React jsx tips. 

  - Code sample for [Feb. React Meetup!](http://www.meetup.com/ReactLA/events/223340763/)
  - Recommend this [react chrome plugin](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)

Comments in jsx
----------

```
    render() {
      return (
        <div>
          <!-- This doesn't work! -->
        </div>
      )
    }
```


```
    render() {
      return (
        <div>
            {
              // this is a comment
            }

            {/* 
              Multi
              line
              comment
            */}  
            
            
            {
              // this is a comment
              // this is a comment
              // this is a comment
            }
        </div>
      )
    }
```

