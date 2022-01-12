---
title: Invoke didSet when property’s value is set inside init context
toc: true
branch: master
categories: [swift-tips, didSet, property-observers]
badges: true
comments: true
layout: post
---

Property observers are only called when the property’s value is set outside of initialization context.

`defer` can change situation 😊

```
class Member {
    var ageMember: Int! {
        didSet {
            print("Function: \(#function)")
        }
    }

    init(age: Int) {
        self.ageMember = age
    }
}

class User {
    var ageUser: Int! {
        didSet {
            print("Function: \(#function)")
        }
    }

    init(age: Int) {
        defer {
            self.ageUser = age
        }
    }
}

Function: ageUser
```

