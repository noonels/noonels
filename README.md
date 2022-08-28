# Hi there, I'm Cooper! 👋

<h2 align="center">About Me</h2>

```f95
! Outputs:
!
! M. Cooper Healy -- Introduction
! Summary:                Endlessly curious, endlessly eager to tell you about it
! Currently Working On:   Teaching myself the ins and outs of Scientific Computing -- mostly using Fortran and Julia
! Looking to Collaborate: .true.
! Contact Info:
!         Github:   github.com/noonels
!         LinkedIn: linkedin.com/in/cooper-healy-a6140718a/
!         Email:    m.cooper.healy@gmail.com

!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

module bio_m
    use iso_varying_string, only: varying_string

    type :: contact_info_t
        type(varying_string) :: github
        type(varying_string) :: linkedIn
        type(varying_string) :: email
    end type

    type :: bio_t
        type(varying_string) :: summary
        type(varying_string) :: current_project
        logical :: looking_to_collaborate
        class(contact_info_t), allocatable :: contact_info

    contains
        private
        procedure, public :: print_introduction
    end type

contains

    subroutine print_introduction(self)
        class(bio_t), intent(inout) :: self

        print *, 'Summary:\t', self%summary
        print *, 'Currently Working On:\t', self%current_project
        print *, 'Looking to Collaborate:\t', self%looking_to_collaborate
        print *, 'Contact Info:'
        print *, '\tGithub:\t', self%contact_info%github
        print *, '\tLinkedIn:\t', self%contact_info%linkedIn
        print *, '\tEmail:\t', self%contact_info%email

    end subroutine

end module

program introduction
    use bio_m, only: bio_t, contact_info_t

    type(bio_t) :: bio

    print *, 'M. Cooper Healy -- Introduction'

    bio = bio_t(&
        summary = 'Endlessly curious, endlessly eager to tell you about it', &
        current_project = 'Teaching myself the ins and outs of Scientific Computing -- mostly using Fortran and Julia',&
        looking_to_collaborate = .true.,&
        contact_info = contact_info_t(&
            github = 'github.com/noonels', &
            linkedIn = 'linkedin.com/in/cooper-healy-a6140718a/', &
            email = 'm.cooper.healy@gmail.com'&
            )&
        )

    call bio%print_introduction()

end program

```

<h2 align="center">How to Reach Me</h2>

<p align="center">

  <a href="https://www.linkedin.com/in/matthew-healy-a6140718a/">
    <img src="https://www.vectorlogo.zone/logos/linkedin/linkedin-icon.svg" alt="M Cooper Healy's LinkedIn Profile" height="30" width="30">
  </a>

  <a href="https://stackoverflow.com/users/story/13262508">
    <img src="https://www.vectorlogo.zone/logos/stackoverflow/stackoverflow-icon.svg" alt="M Cooper Healy's Stack Overflow Profile" height="30" width="30">
  </a>

  <a href="https://meta.stackexchange.com/users/1088743/matthew-healy">
    <img src="https://www.vectorlogo.zone/logos/stackexchange/stackexchange-icon.svg" alt="M Cooper Healy's Stack Exchange Profile" height="30" width="30">
  </a>

  <a href="https://stackshare.io/cooper-healy">
    <img src="https://cdn.worldvectorlogo.com/logos/stackshare.svg" alt="M Cooper Healy's StackShare Profile" height="30" width="30">
  </a>
</p>
