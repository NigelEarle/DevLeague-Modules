# Deployment

## Prerequisites
This material should come after creating a fully featured deployable web application. Students should already be familiar with basic linux commands.

## Class Format / Time to Allow for Subject
This material usually takes XXX to introduce and up to XXX of exercises and reinforcement.

## Topics & Expected Outcomes

#### Levels of Understanding
Students will have *one of three* levels of understanding about each topic upon completion of this module.
- **grok**: fully understand the topic in order to replicate code, communicate, and explain concepts without referring to any notes.
- **explain**: understand enough about the topic to describe concepts without referring to notes.
- **know about**: understand enough to look up further documentation when asked about the subject.

---

- Students should *be able to explain* XXX
- Students should *know about* XXX
- Students should *fully grok* XXX

# Suggested Format for Delivery
The following format is meant to be a guideline for effective delivery. Instructors can present material in another way if it is more effective for the students.

1. Discuss the role of servers in web application architecture
1. What is DevOps?
1. What is deployment?
1. What happens when a user visits google.com?
1. Talk on linux security
1. Linux security, users (root and creation)
1. Linux security, File permissions
1. Linux security, User Group ownership
1. Ports
1. Talk on network security
1. Create admin user
1. ssh keys
1. Deploy static site
1. Deploy node app
1. Talk on automation
1. Talk on high availability
1. Deploy your app!

# Instructor Notes for Each Topic

### What is DevOps?
At the end of this lecture, students should *know about* the following:

1. Security
1. Deployment
1. Automation
1. Availability
1. Scalability

### What is deployment?
At the end of this lecture, students should *be able to explain* web application deployment concepts.

1. Different deployment envs
    1. local developmnt
    1. private alpha staging
    1. public beta uat
    1. public production
1. making your app available to one of these set of users
1. initial set up of server
1. developing a strategy for updating codebase
    1. manual, scp
    1. manual, git
    1. automated, git
    1. automated CD

### What happens when a user visits google.com?
At the end of this lecture, students should *be able to explain* web request and response flow from the networking perspective.

1. DNS resolution as a client
1. Browser request cycle
    1. concurrency limit
1. Setting up DNS
    1. registrar
    1. ns records
    1. dns records

### Talk on linux security
At the end of this lecture, students should *know about* basic concepts of minimal linux server security.

1. never run as root
1. limiting access, deny all by default, allow

### Linux security, users (root and creation)
At the end of this lecture, students should *fully grok* not running anthing as root and *be able to explain* the `sudo` command.

### Create admin user
At the end of this lecture, students should *be able to explain* linux user management and permissions.

### Linux security, File permissions
At the end of this lecture, students should *be able to explain* reading and setting linux file permissions.

### Linux security, User Group ownership
At the end of this lecture, students should *be able to explain* linux user and group ownership of files and directories.

### Ports
At the end of this lecture, students should *be able to explain* what ports are and their role in servers.

### Talk on network security
At the end of this lecture, students should *know about* basic VPS security through limiting access to ports.

Notes for Instructor:
- login to personally provisioned ubuntu container (see SoftCoreOS)
- run this part as a workshop
- read through the `NOTES` file on SoftCoreOS

### SSH Keys
At the end of this lecture, students should *be able to explain* how to securely log in to a shell on a VPS.

### Deploy a Static Site
At the end of this lecture, students should *be able to explain* how to setup nginx as an http web server.

### Deploy a Node App
At the end of this lecture, students should *be able to explain* how a node app runs on a VPS and how to setup nginx as a reverse proxy.

### Talk on Automation
At the end of this lecture, students should *know about* Continuous Integration and Continuous Delivery concepts.

### Talk on High Availability
At the end of this lecture, students should *know about* High Availability concepts.

### Deploy your App!
At the end of this lecture, students should *know about* web application deployment.

### SoftCoreOS
`SoftCoreOS` is the DevLeague student staging box set up on the subdomain softcoreos.devleague.com. All docker commands and notes are on the server in `~/NOTES` file.

# Additional Resources

#### Basic VPS Deployment Resources
- Link: [https://github.com/devleague/Basic-VPS-Deployment-Resources](https://github.com/devleague/Basic-VPS-Deployment-Resources)
- Concepts: nginx configuration
- Notes: Use as reference

