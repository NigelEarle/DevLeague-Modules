# Security

## Suggested order of delivery

1. Talk about security as it relates to web application development
    1. what you should be concerned about
1. Talk about password security
1. Talk about Crypto Hash functions
1. Do the Crypto Hash workshop
1. Do TubeHacked exercise

_do not deliver **More Security Topics**_

## Topics

- Password security [teach]
- Crypto Hashes [teach]
- Good Crypto Hashes [teach]
- Salting Hashes [teach]
- Bruteforce attacks [teach]
- Rainbow table attacks [about]
- Using sensitive data in applications [teach]

## Acceptance

- Students should be scared (thus overly careful) when dealing with sensitive data
- Students should be pessimistic about their security, and work as if an attacker _will_ gain access
- Students should understand the fundamentals, and usage of hash functions
- Students should know the 5 properties of a crypto hash function
- Students should know the 2 additional rules of using good crypto hash functions
- Students should never roll their own crypto algorithms
- Students should understand and be able to communicate good password policy
- Students should understand and be able to demonstrate hashing passwords
- Students should understand and be able to demonstrate salting hashed passwords
- Students should know about bruteforce attacks and why it's feasible against weak passwords
- Students should know about salted hashes and why it's used to counter rainbow table attacks
- Students should know how to use ENV variables in cli
- Students should know how to prevent ENV variables from being saved to shell history
- Students should know how to use .env files
- Students should know how to use .env-sample files
- Students should never commit .env files
- Students are allowed to commit .env-sample files that contain no sensitive information
- Students should never commit sensitive data
- Students should know they can rotate their security keys in case they do
- Students are not expected to become security experts or cryptographers
- Students will gain the mastery of being careful and following maximum best security practices

## Slides (none)

## Work

1. tmp directory `crypto_hashing/index.js` (during workshop)
1. Activity: TubeHacked (no github link yet)


## Crypto Hash Functions

### Workshop

1. perform md5sum and shasum hashes using cli
    1. piping output and files
1. generating hashes in node
    1. using different algorithms


### Talking Points

#### Why use hash functions

1. to quickly compare

#### What are hash functions

- hash function which takes an input (or 'message') and returns a fixed-size alphanumeric string, which is called the hash value
- take arbitrary length and distribute to something smaller

#### parts of hashing

- message
    - can be anything, binary, utf8, image, string, file...
- function
    - takes in a message
    - outputs a message digest
    - one way hash
- digest (aka message digest, aka hash)

#### 5 traits of a crypto hash function

1. simple/fast to create a hash digest from a message
1. one way : mathematically infeasable to construct the message from the digest
1. same message will always produce same digest
1. changing the message changes the digest _dramatically_
1. mathematically infeasable for collisions to occur

#### Good crypto hashes

1. are not meant to be fast
1. are salted

#### Rainbow tables and salting

- whiteboard
- provide examples of where to store salt strings

#### Never commit sensitive data

1. using .gitignore
1. using git-crypt
1. using ENV vars in cli
    1. hiding ENV vars from history
1. using .env files

## Additional Resources

there are no additional resources yet

### More Security topics

can be found in [Deployment](../Deployment) module

such as linux file permissions, user and group ownership
