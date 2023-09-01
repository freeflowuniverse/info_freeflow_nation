# markdown spice

Can be used in circles, code, text, ...

## generic concepts

### Duration

how to specify a duration e.g. in X time from now: 

```1h, 1d, 1w, 1m, 1y (hour,day,min,week, month, year)```

so if you want to say duration is 1 hour use ```1h```

- Time from now is ```+1h``` , just use + in front,
  - when history use - e.g. ```-1m``` means one month ago
  - when you put this in e.g. wiki on relevant part, will be replaced by absolute time

### Date/Time

```bash
#month is first !!!, we always go biggest then to smallest
10/5
#same as previous
10/05
#if year is needed
2023/10/5
#seconds are not used, always hours then minutes, so also biggest one first (hour)
10/5 20:10
```

## INFORMATION

```
#always starts with !!
!!PROJECT id:10 name:aname descr:'my description' deadline:12/5
!!CIRCLE name:mycircle descr:'my circle' members:despiegk,delandtj stakeholders:libor
#can be multi line
!!CIRCLE name:mycircle descr:'my circle' 
    members:despiegk,delandtj 
    stakeholders:libor
#multiline text is also supported
!!CIRCLE 
    name:mycircle 
    descr:
        this is now multiline text
        next line
    members:despiegk,delandtj 
    stakeholders:libor
#lists can also be done multiline, tool is smart enough to figure out the difference
#especially useful for list of longer fields e.g. url's
!!CIRCLE 
    name:mycircle
    members:
        despiegk
        delandtj 
```

generic concepts

- !! specifies its a piece of data, needs to be always at start of line
- the first word (capital insensitive, but try to use uppercase), which object it is
- then the fields, they are different per object e.g. name:...
- when list use comma's
- when space inside the name, descr: need to use '' around

### Objects

every object always has a name and id.

#### USER

- name
- alias []string
- descr


#### PROJECT

- name
- alias []string
- descr
- deadline (date)
- circles (list of circlenames) : []string

#### CIRCLE

Group of people, can be with or without stories, issues, ...

Properties

- main properties
  - name
  - alias []string
  - descr  
  - children []string //children circles, can be more than 1
- how is circle created (this allows you to specify how circle is constructed)
  - admins           []string
  - coordinators     []string
  - members          []string
  - stakeholders     []string
  - watchers         []string
  - contributors     []string

#### STORY

- name
- circles []string      //circles this story belongs too
- alias []string
- descr
- priority (low,high,normal)
- urgency (today,tomorrow,week,2week,month,quarter,year)
- deadline (date)
- owners            []string    //responsiblity it gets done
- contributors      []string
- watchers          []string   //they want to be informed
- effort            //e.g. 1d or 1h (see duration above)
- depends           []string   //which other stories it depends on


the coordinators, contributors or watchers need to be alias or name

#### ISSUE

- name
- circles []string      //circles this issue belongs too (optional, if story used then circle not needed)
- stories []string      //stories this story belongs too (an issue needs to be linked to circle or story)
- type (bug,fr,question,task)
- descr
- priority (low,high,normal)
- urgency (today,tomorrow,week,2week,month,quarter,year)
- deadline (date)
- owners            []string
- contributors      []string
- watchers          []string   //they want to be informed

#### REQUIREMENT

- name
- products []string     //products this requirement belongs too (needs to be product:version e.g. zos1.0.0)
- stories []string      //stories this requirement belongs too 
- descr
- priority (low,high,normal)
- deadline (date)
- owners            []string
- watchers          []string   //they want to be informed


#### TASK

- name
- stories []string      //stories this story belongs too, needs to be one
- descr
- priority (low,high,normal)
- deadline (date)
- owners            []string
- watchers          []string   //they want to be informed
- effort            //e.g. 1d or 1h (see duration above)
- depends           []string   //which other tasks or stories it waits for


#### PRODUCT

- name
- descr
- owners            []string
- watchers          []string    //they want to be informed
- children          []string    //which product is behind
- links             []string    e.g. github repo link, ...
- depends           []string   //which other tasks or stories it waits for


#### PRODUCTVERSION

- product               //name of the product
- version               //e.g. 1.0.0
- descr
- priority (low,high,normal)
- state                 //new,devel(opment),test(ing),done,arch(ived)
- deadline (date)
- issues []string       //issues this product is related too
- reqs []string         //requirements this product is related too
- stories []string      //stories this product is related too
- circles []string      //circles this product is related too
- effort                //e.g. 1m 
- depends               []string   //which other product versions it depents on

Specific version of the product

#### BLOG

- name
- title
- authors           []string
- descr
- tags              //e.g. technology,dubai
- circles           []string    //if linked to circle(s)
- products          []string    //if linked to products(s)
- links             []string    //e.g. github repo link, ...



### Remarks

the coordinators, contributors or watchers need to be alias or name


## TODO







date notation: -1d, -1w (means 1 day ago, 1 week ago), 12/2 (day/month, no need to do year)