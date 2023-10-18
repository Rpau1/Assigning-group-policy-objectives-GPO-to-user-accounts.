# Assigning-group-policy-objectives-GPO-to-user-accounts.

- Make a Group Policy Object(GPO)

- Add a policy(removes the clock from the task bar in user account) in that GPO.

- Make an Orgonizational Unit(OU).

- Add an user to it.

- Link the new GPO to that OU

*This builds upon the previous System Administration project we did on the Active Directory.

1) Log into the DC VM as an administrtor and open up  server manager.
2) Next, creating GPO: Tools>group policy management console>expand domain> expand group policy object> right click on group policy object> new> name it "Sample1 GPO"
3) Editing GPO: right click on newly created GPO "Samplle GPO">(we are going to hide the clock from the user computer) so expand user configuration > expand administrator template>open start menu and task bar>on the right find the right remove clock setting> doube click on the setting> now enable it>apply>ok>close> click on setting> it will generate a report>add>add>close.
  ![setting comp config gpo 1](https://github.com/Rpau1/Assigning-group-policy-objectives-GPO-to-user-accounts./assets/147562929/88a467ec-f236-482b-a2f0-789486f5917d)
  ![going to server manager and task bar 2](https://github.com/Rpau1/Assigning-group-policy-objectives-GPO-to-user-accounts./assets/147562929/abc9d9d1-c19a-41f2-8076-2067b3155225)
  ![enabiling the rule 3](https://github.com/Rpau1/Assigning-group-policy-objectives-GPO-to-user-accounts./assets/147562929/71f312e7-26a3-4803-9c05-14e13c057c33)
  ![showing gpo 4](https://github.com/Rpau1/Assigning-group-policy-objectives-GPO-to-user-accounts./assets/147562929/5fac427b-57ea-4ff6-9805-0762d3379e9e)

5) Now that the GPO with a policy exists we need to connect it to a orgonizational unit with users in it.
6) right click on domain>new orgonizational unit(OU)> name it "rj" or whatever you like > right click on it> move the user from the user acoount> go to user> find user> right click and move to "rj" or drag>now the user is within the new OU.
    ![getting user name](https://github.com/Rpau1/Assigning-group-policy-objectives-GPO-to-user-accounts./assets/147562929/d4537518-a7d2-4e60-89f3-b723c5b7a386) 
7) to connect an existing group plicy to OU: right click on the OU>link existing group policies>select sample 1 GPO> add> close.
8) The selected user in that OU will have their clock removed from the Task bar.As an example here is my user account rpaul.
     ![final result from removing the clock](https://github.com/Rpau1/Assigning-group-policy-objectives-GPO-to-user-accounts./assets/147562929/8630891f-eca2-4cd2-8023-5c129589ea77)
