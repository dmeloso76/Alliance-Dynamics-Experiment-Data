# Alliance-Dynamics-Experiment-Data

This folder contains two csv files. GAdata.csv contains per-subject/ per-period data on decisions made by participants in all our sessions. Interaction_Data.csv contains data aggregated by interactions. E.g., fraction of periods during which an interaction cooperated.

### File GAdata.csv, variables
This data set contains one data point for each choice made by every subject that participated in the experiment.

* Session: session ID, from 1 to 16.
* Subject: session-specific subject ID, from 1 to 24 in most sessions.
* GovStructure: governance structure of the alliance. Four possible values:
    * 2-player: two players, no exit cost.
    * 3-player: three players, no exit cost.
    * 2-Exit cost: two players, exit cost.
    * 3-Exit cost: three players, exit cost.
* Game: the strategic properties of the alliance game played. Either CG, for coordination game, or PD, for prisoner's dilemma.
* interactionDraw: the number of periods per interaction was randomly drawn in the first two sessions, and replicated afterwards. There are thus two types of ``interaction draws''. Type 1 has seven interactions, lasting 5, 14, 5, 11, 6, 12, and 37 periods each. Type 2 has six interactions, lasting 19, 4, 2, 15, 20, and 21 periods each.
* interaction: session-specific interaction ID. For type 1 interaction draw, the ID goes from 1 to 7, for type 2 interaction draw it goes from 1 to 5.
* Period: interaction-specific period ID, ranging from 1-2 in the shortest interaction, to 1-37 in the longest interaction.
* Partnership: alliance ID. In each interaction of a session, two or three subjects interact repeatedly. Partnership is the interaction-specific ID of the group interacting repeatedly.
* Profit: profit obtained by the given subject in the current interaction and period.
* Matchpay: cumulative profit obtained by the given subject in the current interaction up to the current period.
* Finished: if equal to 0, the current alliance has not been terminated by a partner exiting. Is larger than 0, the current alliance has been terminated in the specified period by a partner exiting.
* Choice: action chosen by the subject in the current interaction and period. Five possible values: C means the subject contributes resources to the alliance, nC means the subject does not contribute resources to the alliance, E means the subject chooses to exit the alliance, E- means the subject or one of her partners chose to exit the alliance in a preceding period.
* Terminator: a dummy that takes on the value of 1 if the alliance was terminated by the subject's choice to exit in the current or some preceding period. If, instead, the alliance has not been terminated, or it was terminated by a partner's choice to exit, the dummy equals 0.
* PartnerChoice.Poc: choice of the single partner in two-player alliances. Choice of ``partner one'' in three-player alliances.
* PTc: empty for two-player alliances. Choice of ``partner two'' in three-player alliances.
* gplay: indicator of joint choice of all alliance partners.\
It takes on 7 different values for two-player alliances: 1 if both choose C, 2 if the subject chooses C and her partner nC, 4 if the subject chooses nC and her partner C, 6 if both subjects choose nC, 7 if the subject chooses E, 8 if the subject's partner chooses 8, and 9 in all other cases. \
It takes on 9 different values for three-player alliances: 1 if all players choose C, 2 if the subject and one partner choose C while another partner chooses nC, 3 if the subject chooses C and both partners choose nC, 4 if the subject chooses nC and both partners choose C, 5 if the subject and one partner choose nC while another partner chooses C, 6 if all three players choose nC, 7 if the subject chooses E, 8 if a partner chooses E, 9 in all other cases.
* simplay: indicator of joint choice of all partners, treats partners symmetrically.\
For two-player alliances, the values are: 1 if both choose C, 2 if one partner chooses C and the other nC, 4 if both choose nC, 5 if one partner chooses E, 6 if E was chosen in some preceding period.\
For three-player alliances, the values are: 1 if all partners choose C, 2 if two partners choose C and one partner chooses nC, 3 if two partners choose nC and one partner chooses C, 4 if all partners choose nC, 5 if one partner chooses E, 6 if E was chosen in some preceding period.
* Age: age of the subject, as collected from the exit questionnaire.
* Gender: gender of the subject, as collected from the exit questionnaire.

### File Interaction_Data.csv
This data set contains one data point for each interaction formed by sets of two or three subjects during all sessions of the experiment.

* Session: session ID, from 1 to 16
* interaction: session-specific interaction ID. For type 1 interaction draw, the ID goes from 1 to 7, for type 2 interaction draw it goes from 1 to 5.
* Partnership: alliance ID. In each interaction of a session, two or three subjects interact repeatedly. Partnership is the interaction-specific ID of the group interacting repeatedly.
* gstruct: governance structure of the alliance. Four possible values:
    * 2-player: two players, no exit cost.
    * 3-player: three players, no exit cost.
    * 2-Exit cost: two players, exit cost.
    * 3-Exit cost: three players, exit cost.
* game: the strategic properties of the alliance game played. Either CG, for coordination game, or PD, for prisoner's dilemma.
* it_type: the number of periods per interaction was randomly drawn in the first two sessions, and replicated afterwards. There are thus two types of ``interaction draws''. Type 1 has seven interactions, lasting 5, 14, 5, 11, 6, 12, and 37 periods each. Type 2 has six interactions, lasting 19, 4, 2, 15, 20, and 21 periods each.
* it_length: length, in periods, of the current interaction.
* fins: period in which the alliance was terminated because a partner chose E. If equal to 0, the alliance was never terminated.
* Ldum: a dummy, specified as a factor variable equal to "CC last period" if all partners chose C in the last period of the interaction, or "not CC last period" if not all partners chose C in the last period of the interaction.
* startC: conditional on all partners chosing C in the last period, startC gives the first period when C was chosen by all partners, to keep on being chosen until the final period of the interaction. startC = 0 means partners did not all choose C in the last period.
* cfreq: fraction of all periods of the interaction in which all partners jointly chose C.
* ncfreq: fraction of all periods of the interaction in which all partners jointly chose nC.
* fcdummy: dummy, equal to 1 if all partners chose C in all periods of the interaction.
* sdummy: dummy equal to 1 if an alliance is "successful", meaning that all partners choose C in all periods. Its value is 0 otherwise.
* tdummy: dummy, specified as a factor variable equal to "Terminated" if the alliance was terminated by a partner choosing E in some period, and "Never E" if no partner chose E in any period.
* simple: dummy, specified as a factor variable equal to "2-player" if the governance structure is 2-player, and "Other" otherwise.
* exitcost: dummy, specified as a factor variable equal to "2-Exit cost" if the governance structure is 2-Exit cost, and "Other" otherwise.
* multi: dummy, specified as a factor variable equal to "3-player" if the governance structure is 3-player, and "Other" otherwise.
* multec: dummy, specified as a factor variable equal to "3-Exit cost" if the governance structure is 3-Exit cost, and "Other" otherwise.

