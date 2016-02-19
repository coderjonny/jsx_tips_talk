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

Mapping Arrays in jsx
----------

```
//one liner
{ this.props.people.map( person => <div> {person} </div> ) }

// multiline use a return
{ this.props.people.map( person => {
  return (
    <div className="col-sm-1">
      <img src={person}
           style={{
                  width: 80,
                  height: 80,
                  margin: '10px 0'
                  }}
           className="img-rounded" /> 
    </div>
  )
}) }

```

Contitionals in jsx
----------

```
let tooMany = (people) => { this.props.people.length > 10 }

{ tooMany(people) && this.props.people.map( person => {
  return (
    <div>
      { person }
    </div>
  )
}) }

```


Ternary statements in jsx
----------

```
let tooMany = (people) => { this.props.people.length > 10 }

{ tooMany(people)? 
      <PeopleList />
      :
      <div> sorry too many people </div>
}

```